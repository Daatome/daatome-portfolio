<script setup>

import {ref} from 'vue'
import Badge from './Badge.vue';

const ibm= ref("ibm.png")
const igem= ref("igem.png")
</script>


<template>
    <div class="container mx-auto bg-white shadow-lg rounded-lg p-10 ">
        <h1 class=" text-3xl border-b-4 border-emerald-500 pb-3">Insignias y Reconocimientos</h1>
        <Badge
            :image="ibm"
        >
            <template v-slot:titulo>
                <h1 class="text-2xl mb-5 font-semibold">IBM Z Xplore - Concepts</h1>

            </template>
            <template #descripcion>
                <p>El acreedor  de la insignia ha aprendido y demostrado las habilidades fundamentales de IBM Z y comprende los conceptos de IBM Z. Esta persona es capaz de realizar tareas cotidianas en un entorno IBM Z, incluida la administración de conjuntos de datos, la formulación de comandos, la gestión de JCL, la programación de acciones en USS (Unix System Services), la escritura y la depuración de Python y la orquestación de acciones a través de IBM Z Open Automation Utilities.</p>

            </template>
        </Badge>
        <Badge
            :image="igem"
        >
            <template v-slot:titulo>
                <h1 class="text-2xl mb-5 font-semibold">IGEM Competition</h1>

            </template>
            <template #descripcion>
                <p>El acreedor  de la insignia ha aprendido y demostrado las habilidades fundamentales de IBM Z y comprende los conceptos de IBM Z. Esta persona es capaz de realizar tareas cotidianas en un entorno IBM Z, incluida la administración de conjuntos de datos, la formulación de comandos, la gestión de JCL, la programación de acciones en USS (Unix System Services), la escritura y la depuración de Python y la orquestación de acciones a través de IBM Z Open Automation Utilities.</p>

            </template>
        </Badge>
        
    </div>
</template>


<style  scoped>

</style>