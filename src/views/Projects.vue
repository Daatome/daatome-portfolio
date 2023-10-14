
<script setup>
import {ref, reactive, onMounted} from 'vue'

import Proyectos from '../components/Proyectos.vue';
import Proyecto from '../components/Proyecto.vue';

const pMaraly=reactive({
    name:"Constructora Maraly",
    folder:"maraly",
    images:[
        "maraly1.jpg",
        "maraly2.jpg",
        "maraly3.jpg",
        "maraly4.jpg",
        "maraly5.jpg",
        "maraly6.jpg",
        "maraly7.jpg",
        "maraly8.jpg",
    ],
    descripcion: "Hola esta es la descripcion del proyecto",
    link:"https://gcmaraly.netlify.app/#/"
})
const pSdip=reactive({
    name:"Sistema Divisional de Información y Planeación (SDIP CSH)",
    folder:"sdip",
    images:[
        "sdip1.jpg",
        "sdip2.jpg",
        "sdip3.jpg",
        "sdip4.jpg",
    ],
    descripcion: "Hola esta es la descripcion del proyecto",
    link:"https://infocsh.izt.uam.mx/sdiplaravel/"
})
const pIgem=reactive({
    name:"IGEM UAM",
    folder:"igem",
    images:[
        "igem1.png",
        "igem2.png",
        "igem3.png",
        "igem4.png",
        "igem5.png",
        "igem6.png",
    ],
    descripcion: "Hola esta es la descripcion del proyecto",
    link:"https://2022.igem.wiki/uam/index.html"
})
const pInovac=reactive({
    name:"Inovac ",
    folder:"inovac",
    images:[
        "inovac1.png",
        "inovac2.png",
        "inovac3.png",
        "inovac4.png",
        "inovac5.png",
    ],
    descripcion: "Hola esta es la descripcion del proyecto",
    link:"https://daatomeinovac.netlify.app/"
})

const pReparalia=reactive({
    name:"Reparalia ",
    folder:"reparalia",
    images:[
        "reparalia1.png",
        "reparalia2.png",
        "reparalia3.png",
        "reparalia4.png",
        "reparalia5.png",
        "reparalia6.png",
        "reparalia7.png",
        "reparalia8.png",
        "reparalia9.png",
        "reparalia10.png",
        "reparalia11.png",
        "reparalia12.png",
    ],
    descripcion: "Hola esta es la descripcion del proyecto",
    link:"https://github.com/CristofAG/Reparalia"
})

const proyectos = ref([pSdip,pMaraly,pIgem,pReparalia,pInovac])
</script>
<template>
    <h1 class="text-3xl font-bold mt-10 text-center">Proyectos en los que he participado</h1>
    <div class="container mx-auto  bg-white shadow-lg ">
    
    
        <Proyectos class="mt-10">
            <Proyecto v-for="proyecto in proyectos" :project="proyecto">
            </Proyecto>
        </Proyectos>
    </div>
</template>

<style lang="scss" scoped>

</style>