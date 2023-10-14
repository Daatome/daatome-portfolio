
<script setup>
import {  ref ,computed} from 'vue';

import { Navigation, Pagination, Scrollbar, A11y, Autoplay } from 'swiper/modules';

import {Swiper, SwiperSlide} from 'swiper/vue'

import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import 'swiper/css/scrollbar'
import 'swiper/css/bundle'
import 'swiper/css/autoplay'
const modules=ref([Navigation, Pagination, Scrollbar, A11y,Autoplay])



const props=defineProps({
    
    project:{
        type:Object,
        required:true
    }

})


</script>

<template class=" mb-10">
    <div class="  bg-white  container mx-auto mb-10  border-gray-300 p-10 border-b-4 my-4">
        <div class="mx-10 mt-5 md:flex  items-center justify-between">
                
            <div class="md:flex-auto md:w-8/12 ">

                <Swiper 
                    :modules="modules"
                    :slides-per-view="1.2"
                    :space-between="10"
                    :loop="true"
                    @swiper="onSwiper"
                    @slideChange="onSlideChange"
                    :autoplay="{delay: 3000}"
                    
                    
                >
                    <SwiperSlide v-for="image in project.images" class="cursor-grab" >
                        <img :src="`/images/projects/${project.folder}/${image}`" :alt="image" data-modal-target="defaultModal" data-modal-toggle="defaultModal">
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