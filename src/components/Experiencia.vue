<script setup>
import {reactive, ref} from 'vue'

import { Navigation, Pagination, Scrollbar, A11y, Autoplay } from 'swiper/modules';

import {Swiper, SwiperSlide} from 'swiper/vue'

import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import 'swiper/css/scrollbar'
import 'swiper/css/bundle'
import 'swiper/css/autoplay'


const vue= reactive({
    name:'Vue',
    'image':"vue.png"
})
const angular= reactive({
    name:'Angular',
    'image':"angular.png"
})
const bootstrap= reactive({
    name:'Bootstrap',
    'image':"bootstrap.png"
})
const c= reactive({
    name:'C',
    'image':"c.png"
})
const css= reactive({
    name:'css',
    'image':"css.png"
})
const docker= reactive({
    name:'Docker',
    'image':"docker.png"
})
const git= reactive({
    name:'git',
    'image':"git.png"
})
const github= reactive({
    name:'gitHub',
    'image':"github.png"
})
const gitlab= reactive({
    name:'gitLab',
    'image':"gitlab.png"
})
const html= reactive({
    name:'Html',
    'image':"html.png"
})
const java= reactive({
    name:'java',
    'image':"java.png"
})
const js= reactive({
    name:'javaScript',
    'image':"js.png"
})
const laravel= reactive({
    name:'laravel',
    'image':"laravel.png"
})
const leaflet= reactive({
    name:'Leaflet',
    'image':"leaflet.png"
})
const livewire= reactive({
    name:'Livewire',
    'image':"livewire.png"
})
const mongo= reactive({
    name:'Mongo',
    'image':"mongo.png"
})
const mysql= reactive({
    name:'Mysql',
    'image':"mysql.png"
})
const php= reactive({
    name:'Php',
    'image':"php.png"
})
const sass= reactive({
    name:'Sass',
    'image':"sass.png"
})
const spring= reactive({
    name:'Spring',
    'image':"spring.png"
})
const tailwind= reactive({
    name:'Tailwind',
    'image':"tailwind.png"
})

const modules=ref([Navigation, Pagination, Scrollbar, A11y,Autoplay])


const tecnologies=ref([laravel, vue,angular,bootstrap,c,css,docker,git,github,gitlab,html,java,js,leaflet,livewire,mongo,mysql,php,sass,spring,tailwind])
</script>

<template>
    <div class=" container mx-auto mb-10">

        <h1 class="text-3xl text-center">Tecnologias con las que he trabajado</h1>
        <div class="mt-10 ">

            <Swiper 
                    :modules="modules"
                    :slides-per-view="5"
                    :space-between="10"
                    :loop="true"
                    @swiper="onSwiper"
                    @slideChange="onSlideChange"
                    navigation
                    :scrollbar="{ draggable: true }"
                    :autoplay="{delay: 3000}"
                    
            >
                <SwiperSlide v-for="tecnology in tecnologies" class="cursor-grab p-10 "
                    
                >

                    <h2 class="md:text-2xl text-xs text-center   mb-0 ">{{tecnology.name}}</h2>
                    <h3 class=" border-emerald-500  border-b-4 mb-10 block px-8"></h3>
                    <img :src="`/images/tecnologies//${tecnology.image}`" :alt="tecnology.name" class="mb-10  rounded-xl">

                </SwiperSlide>
                    
            </Swiper>
        </div>

    </div>
</template>



<style  scoped>

</style>