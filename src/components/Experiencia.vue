<script setup>
import {reactive, ref} from 'vue'

import { Navigation, Pagination, Scrollbar, A11y } from 'swiper/modules';

import {Swiper, SwiperSlide} from 'swiper/vue'

import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import 'swiper/css/scrollbar'
import 'swiper/css/bundle'

const laravel= reactive({
    name:'Laravel',
    'image':"laravel.jpg"
})
const vue= reactive({
    name:'Vue',
    'image':"vue.png"
})

const tecnologies=ref([laravel, vue])
</script>

<template>
    <div class="container mx-auto mb-10">

        <h1 class="text-3xl text-center">Tecnologias con las que he trabajado</h1>
        <div class="mt-10 ">

            <Swiper 
                    :modules="modules"
                    :slides-per-view="5"
                    :space-between="50"
                    :pagination="true"
                    :autoplay="autoplay"
                    :loop="true"
                    
            >
                <SwiperSlide v-for="tecnology in tecnologies" class="cursor-grab flex justify-center align-middle">

                    <img :src="`/images/tecnologies//${tecnology.image}`" :alt="tecnology.name" class="  rounded-xl">
                    <h2 class="text-2xl text-center  block">{{tecnology.name}}</h2>

                </SwiperSlide>
                    
            </Swiper>
        </div>

    </div>
</template>



<style  scoped>

</style>