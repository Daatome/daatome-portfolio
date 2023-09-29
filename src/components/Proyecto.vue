
<script setup>
import {  ref } from 'vue';


import { Navigation, Pagination, Scrollbar, A11y } from 'swiper/modules';

import {Swiper, SwiperSlide} from 'swiper/vue'

import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import 'swiper/css/scrollbar'
import 'swiper/css/bundle'

const imagesMaraly= ref([
    "maraly1.jpg",
    "maraly2.jpg",
    "maraly3.jpg",
    "maraly4.jpg",
    "maraly5.jpg",
    "maraly6.jpg",
    "maraly7.jpg",
    "maraly8.jpg",
])

const props=defineProps({
    images:{
        type:Array,
        required:true
    },
    name:{
        type:String,
        required:true
    },
    project:{
        type:Object,
        required:true
    }

})


</script>

<template >
    <div class="  bg-white  container mx-auto mb-10  border-gray-200 p-10 border-b-4 my-4">

        <div class="mx-10 mt-5 md:flex mx-5 items-center justify-between">
                
            <div class="md:flex-auto md:w-7/12 ">

                <Swiper 
                    :modules="modules"
                    :slides-per-view="1.5"
                    :space-between="50"
                    :pagination="true"
                    :autoplay="autoplay"
                    :loop="true"
                    
                >
                    <SwiperSlide v-for="image in project.images" >
                        <img :src="`/images/projects/${project.folder}/${image}`" :alt="image" >
                    </SwiperSlide>
                    
                </Swiper>
            </div>

            <div class="flex-auto md:w-10/12  mt-9 md:mt-0 md:ms-10">
                <h2 class="text-2xl text-emerald-500 font-bold uppercase  border-emerald-500 p-3 border-b-4 my-4">
                    {{ project.name }}
                </h2>
                <p class="text-sm font-semibold mb-9">{{ project.descripcion }}</p>
                <a :href="project.link" target="_blank"
                class="bg-emerald-500 font-bold text-center text-white p-2 mt-10 block rounded-xl hover:bg-emerald-700 hover:text-gray-100">
                    Link al sitio original
                </a>
            </div>
        </div>
        
    </div>
</template>

<style  scoped>


</style>