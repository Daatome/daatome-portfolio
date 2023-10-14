<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { computed ,ref} from 'vue';

import Header from './components/Header.vue';
import Footer from './components/Footer.vue';



</script>

<template >
<div class="bg-gray-200">

    <Header/>
    <RouterView/>
    <Footer/>
</div>

</template>

<style >

</style>
