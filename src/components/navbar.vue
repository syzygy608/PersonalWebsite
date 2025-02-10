<template>
    <nav class = "flex w-full justify-between items-center px-3 h-[3rem] bg-gray-800 text-white">
        <div>
            Han-Ping Wu 吳翰平
        </div>
        <ul class = "md:flex hidden space-x-4">
            <li>
                <a href = "#">Home</a>
            </li>
            <li>
                <a href = "#about">About</a>
            </li>
            <li>
                <a href = "#contact">Contact</a>
            </li>
        </ul>
        <div id="hamburger" @click="showMenu = !showMenu" class = "md:hidden cursor-pointer">
            <svg class = "w-6 h-6" fill = "none" stroke = "currentColor" viewBox = "0 0 24 24" xmlns = "http://www.w3.org/2000/svg">
                <path stroke-linecap = "round" stroke-linejoin = "round" stroke-width = "2" d = "M4 6h16M4 12h16m-7 6h7"></path>
            </svg>
        </div>
        <transition name="slide-fade">
            <ul v-if="showMenu" class="md:hidden space-y-4 absolute text-center top-12 right-0 w-[max(20%,10rem)] bg-slate-800 p-4 z-10">
                <li>
                    <a href = "#">Home</a>
                </li>
                <li>
                    <a href = "#About">About</a>
                </li>
                <li>
                    <a href = "#Contact">Contact</a>
                </li>
            </ul>
        </transition>
    </nav>
</template>

<script setup>
import { ref } from 'vue'

const showMenu = ref(false);



</script>