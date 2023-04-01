<template>
    <section class="relative bg-gray-900 min-h-screen">
        <Navbar/>
        <div class="flex flex-row w-full max-sm:flex-col max-sm:items-center">
            <div class="flex flex-col w-1/2 h-screen pb-24 pl-16 justify-center max-sm:w-11/12 max-sm:pl-0">
                <div class="flex flex-col sm:flex-col sm:justify-center sm:space-y-0">
                    <p class="text-green-700 mb-2">Android Enthusiast Jakarta</p>
                    <h1 class="text-white text-3xl font-bold pb-4">Bootcamp Android Architecture</h1>
                    <p class="text-base text-white font-thin max-sm:text-sm">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat vel exercitationem eos qui veniam illum perspiciatis, sapiente inventore, aspernatur natus quae laborum voluptatum accusantium id illo nesciunt reprehenderit mollitia. Fugit?</p>
                </div>
            
                <div class="mt-0 lg:mt-12 mb-8 lg:mb-24 space-y-4 sm:flex-row sm:justify-center">
                <a href="#" class="inline-flex mr-3 justify-center items-center py-3 px-5 text-base font-medium text-center text-white rounded-lg bg-green-700 hover:bg-green-800 focus:ring-4 focus:ring-green-300 focus:ring-gray-100">
                    Enroll Now
                    <svg class="ml-2 -mr-1 w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                </a>
                <a href="#" class="inline-flex justify-center items-center py-3 px-5 text-base font-medium text-center text-white rounded-lg border border-gray-300 focus:ring-4 focus:ring-gray-100">
                    Download Syllabus
                </a>
                </div>
            </div>
            <div class="flex flex-col w-1/2">
               
            </div>
        </div>
    </section>

    <section class="relative bg-gray-800 rounded-bl-[100px] max-sm:rounded-none">
        <div class="flex w-full justify-center items-center">
            <div class="flex flex-row max-sm:flex-col w-11/12 max-sm:mt-4 mt-16 mb-16 max-sm:items-start justify-center items-center">
                <div class="flex flex-col h-32 max-sm:h-24 max-sm:items-start w-1/3 items-center">
                    <div class="flex h-full flex-col pt-2">
                        <p class="text-white text-sm font-bold mb-1">Estimated time 4 Month</p>
                        <p class="text-white mb-2">4 Month</p>
                        <p class="text-white text-sm mb-1">At 10 hrs/week</p>
                    </div>
                </div>
                <div class="flex flex-colw-1/3 h-32 items-center max-sm:items-start border-x max-sm:border-none max-sm:mt-6">
                    <div class="flex flex-col h-full px-16 pt-2 max-sm:px-0">
                        <p class="text-white text-sm font-bold mb-1">Enroll By</p>
                        <p class="text-white mb-2 ">April 5, 2023</p>    
                        <p class="text-white text-sm mb-1 ">Get access to the classroom</p>
                        <p class="text-white text-sm">immediately upon enrollment</p>
                    </div>
                </div>
                <div class="flex flex-col w-1/3 h-32 items-center max-sm:items-start">
                    <div class="flex flex-col h-full ml-10 pt-2 max-sm:ml-0">
                        <p class="text-white text-sm font-bold mb-1">Skills acquired</p>
                        <p class="text-white mb-6 max-sm:mb-4 max-sm:text-sm">Threading, Heap Memory, Dynamic Memory Allocation, Control Flow</p>
                        <a class="text-white text-sm">See more skills+</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
</template>

<script setup>
import Navbar from '../components/Navbar.vue';


</script>