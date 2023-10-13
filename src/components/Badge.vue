
<script setup>
import {  ref } from 'vue';


const props= defineProps({
    image:{
        required: true,
        type: String
    }
})

const imagePath= "/images/badges/"+props.image

</script>
<template>
    <div class="flex justify-center flex-col align-middle md:flex-row my-10 gap-8">
        <div class=" md:w-4/12">
            <img :src="imagePath" alt="">
            
        </div>
        <div class=" md:w-8/12">
            <slot name="titulo"></slot>
            <slot name="descripcion"></slot>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>