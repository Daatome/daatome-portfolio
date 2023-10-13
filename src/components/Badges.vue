<script setup>

import {ref} from 'vue'
import Badge from './Badge.vue';

const ibm= ref("ibm.png")
const igem= ref("igem.png")
const voxy= ref("voxy.png")
const laravel= ref("laravel.png")
</script>


<template>
    <div class="container mx-auto bg-white shadow-lg rounded-lg p-10 my-10">
        <h1 class=" text-3xl border-b-4 border-emerald-500 pb-3 font-bold">Insignias y Reconocimientos</h1>
        <Badge
            :image="ibm"
        >
            <template v-slot:titulo>
                <h1 class="text-2xl mb-5 font-semibold border-b-2 border-gray p-2">IBM Z Xplore - Concepts</h1>

            </template>
            <template #descripcion>
                <p>El acreedor  de la insignia ha aprendido y demostrado las habilidades fundamentales de IBM Z y comprende los conceptos de IBM Z. Esta persona es capaz de realizar tareas cotidianas en un entorno IBM Z, incluida la administración de conjuntos de datos, la formulación de comandos, la gestión de JCL, la programación de acciones en USS (Unix System Services), la escritura y la depuración de Python y la orquestación de acciones a través de IBM Z Open Automation Utilities.</p>

            </template>
        </Badge>
        <Badge
            :image="igem"
        >
            <template v-slot:titulo>
                <h1 class="text-2xl mb-5 font-semibold border-b-2 border-gray p-2">IGEM Competition</h1>

            </template>
            <template #descripcion>
                <p>Formé parte del equipo IGEM-UAM, donde colaboré en un proyecto de biología sintética como parte de un equipo multidisciplinario. Mi labor involucró investigar, desarrollar y presentar los resultados a través de una página web. Como un gran logro, al término de la competencia, nuestro equipo fue galardonado con una codiciada medalla de oro. Esta experiencia en investigación y trabajo en equipo reforzó mi pasión por temas de otras áreas y de igual manera reforzo mi habilidad de comunicación.</p>

            </template>
        </Badge>
        <Badge
            :image="voxy"
        >
            <template v-slot:titulo>
                <h1 class="text-2xl mb-5 font-semibold border-b-2 border-gray p-2">Becalos English Challenge</h1>

            </template>
            <template #descripcion>
                <p>Durante el período 2021-2022, tuve el privilegio de formar parte del programa "Becas Becalos English Challenge". Esta enriquecedora experiencia me permitió mejorar significativamente mis habilidades en el idioma inglés. A través de este desafío, no solo adquirí un mayor dominio del idioma, sino que también fortalecí mis capacidades de comunicación oral y escrita, lo que ha sido fundamental en mi desarrollo académico y personal.</p>

            </template>
        </Badge>


        <Badge
            :image="laravel"
        >
            <template v-slot:titulo>
                <h1 class="text-2xl mb-5 font-semibold border-b-2 border-gray p-2">Laravel</h1>

            </template>
            <template #descripcion>
                <p>Aproveché una oportunidad de aprendizaje en Udemy, donde participé en un curso dedicado a Laravel. Durante este programa, me sumergí en aspectos clave de este framework, incluyendo Blade, que me permitió crear vistas web dinámicas de manera eficiente. También exploré Livewire, una potente biblioteca que mejoró mi capacidad para desarrollar aplicaciones interactivas en tiempo real. Breeze, por otro lado, simplificó la creación de sistemas de autenticación sólidos. Además, adquirí habilidades para la creación de APIs, lo que amplió mi comprensión en la exposición de datos y funcionalidades. Este curso en Udemy ha sido un valioso paso en mi camino hacia la excelencia en el desarrollo web.</p>

            </template>
        </Badge>
        
    </div>
</template>


<style  scoped>

</style>