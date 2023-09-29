<script setup>
import {ref, reactive} from 'vue'

import Proyectos from '../components/Proyectos.vue';
import Proyecto from '../components/Proyecto.vue';


const maraly= ref('maraly')
const igem= ref('igem')
const sdip= ref('sdip')


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

</script>

<template>

    <div class="container mx-auto mt-4">
        <!--Presentation  -->
        <div class="md:flex mx-5 items-center justify-between">
            <div class="flex-auto md:w-4/12  text-4xl mx-12 md:mx-0">
                <img src="images/daniel2.jpg" class="w-60 h-60 object-cover rounded-full " alt="">
            </div>

            <div class="flex-auto md:w-10/12  mt-9 md:mt-0">
                <h1 class="text-3xl mb-5 text-center md:text-start">Mi nombre es <span class="text-emerald-500 font-bold"> Daniel Atonal </span></h1>
                <p >Soy licenciado en Computacion enfocado en el area
                    de desarrollo de software. Tambien tengo experiencia
                    liderando equipos siguiendo metodologías agiles para
                    la entrega continua de resultados.
                </p>
                <p>
                    Constantemente busco profundizar en nuevos conocimientos. Actualmente, desempeño el rol de Scrum Master al liderar un equipo en el desarrollo de una plataforma dedicada a la gestión de datos de estudiantes, profesores y coordinadores (SDIP) en la División de Ciencias Sociales y Humanidades de la Universidad Autónoma Metropolitana - Iztapalapa.
                </p>
            </div>
        </div>
    </div>
    <Proyectos class="mt-10">
        <Proyecto 
            
            :project="pMaraly"
        ></Proyecto>
        <Proyecto 
            
            :project="pSdip"
        ></Proyecto>
    </Proyectos>
</template>


<style  scoped>

</style>