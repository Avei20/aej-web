<script setup>
import Navbar from "../components/Navbar.vue";
import { ref } from "vue";
</script>

<template>

    <section class="relative bg-gray-900">
        <Navbar />
    </section>

    <section class="relative bg-gray-900 w-full rounded-bl-[95px]">
        <div class="flex flex-row w-full items-center">
            <div class="w-1/2 flex flex-col text-white p-16">
                <h1 class="text-4xl font-medium">Individual Learners Catalog</h1>
                <p>Transform your career with Nanodegree programs starting at <span class="font-bold">$399/mo.</span></p>
            </div>
            <div class="flex-1 w-1/ mr-20">
              <label for="default-search" class="mb-2 text-sm font-medium text-gray-900 sr-only dark:text-gray-300">Search</label>
              <div class="relative">
                <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
                  <svg aria-hidden="true" class="w-5 h-5 text-gray-500 dark:text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
                  </svg>
                </div>
                <input type="search" id="default-search" class="block p-4 pl-10 w-full text-sm text-gray-900 bg-white rounded-lg border border-gray-300 focus:ring-green-500 focus:border-green-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-green-500 dark:focus:border-green-500" placeholder="Search Android, Flutter..." required="">
                <button type="submit" class="text-white absolute right-2.5 bottom-2.5 bg-green-700 hover:bg-green-800 focus:ring-4 focus:outline-none focus:ring-green-300 font-medium rounded-lg text-sm px-4 py-2 dark:bg-green-600 dark:hover:bg-green-700 dark:focus:ring-green-800">
                  Search
                </button>
              </div>
            </div>
        </div>
    </section>

    <section class="w-full mt-10 flex justify-center">
        <div class="w-11/12 flex flex-col">
            <div>
                <p class="font-medium">Filter by:</p>
            </div>
            <div class="mt-4">
                <ul class="grid gap-2 grid-cols-6">
                    <MultiSelect v-model="selectedCities" :options="topics" filter optionLabel="name" placeholder="Topic" :maxSelectedLabels="3" class="w-full md:w-20rem" />
                    <MultiSelect v-model="selectedCities" :options="cities" filter optionLabel="name" placeholder="Field" :maxSelectedLabels="3" class="w-full md:w-20rem" />
                    <MultiSelect v-model="selectedCities" :options="cities" filter optionLabel="name" placeholder="Skill Level" :maxSelectedLabels="3" class="w-full md:w-20rem" />
                    <MultiSelect v-model="selectedCities" :options="cities" filter optionLabel="name" placeholder="Duration" :maxSelectedLabels="3" class="w-full md:w-20rem" />
                    <MultiSelect v-model="selectedCities" :options="cities" filter optionLabel="name" placeholder="Price" :maxSelectedLabels="3" class="w-full md:w-20rem" />
                    <MultiSelect v-model="selectedCities" :options="cities" filter optionLabel="name" placeholder="Short By" :maxSelectedLabels="3" class="w-full md:w-20rem" />
                </ul>
            </div>
        </div>
    </section>

    <section class="w-full mt-10 flex justify-center">
        <div class="w-11/12 grid gap-5 grid-cols-2">
            <div class="flex flex-row drop-shadow-2xl bg-gray-50">
                <div class="border-r-2 p-3 w-60">
                    <div class="w-full">
                        <img src="/public/aej-logo.svg" class="w-36 max-md:w-full max-md:h-[300px] bg-green-700  rounded-bl-[55px] h-[130px]" alt="AEJ Logo"/>
                    </div>
                    <div class="flex flex-col sm:flex-col justify-center items-center mt-3">
                        <a href="#" class="flex flex-row py-3 px-5 mb-2 justify-between  items-center w-fit text-sm font-medium text-center text-white rounded-lg bg-green-700 hover:bg-green-800 focus:ring-4">
                            Program Details
                        </a>
                        <a href="#" class="flex w-fit justify-center items-center py-3 px-2 text-sm font-medium text-center text-green-700 rounded-lg border border-green-700 focus:ring-4 focus:ring-gray-100">
                            Download Syllabus
                        </a>
                    </div>
                </div>
                <div class="flex flex-col w-full items-center">
                    <div class="flex flex-col w-full items-center py-6">
                        <div class="flex flex-col w-11/12">
                            <button class="bg-lime-400 px-4 py-2 rounded-full text-xs w-28">Nanodegree</button>
                            <h1 class="text-xl font-semibold pt-4">Introduction to Programming</h1>
                            <p class="text-xs pt-2">A first step for beginers towards careers in web and app development, machine learning, data science, AI and More.</p>
                        </div>
                    </div>
                    <div class="w-full bg-gray-200 flex justify-center mt-8">
                        <div class="flex flex-row justify-between w-11/12 py-4">
                                <div class="flex items-center">
                                    <div class="flex items-center">
                                        <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 640 512"><!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M576 0c17.7 0 32 14.3 32 32V480c0 17.7-14.3 32-32 32s-32-14.3-32-32V32c0-17.7 14.3-32 32-32zM448 96c17.7 0 32 14.3 32 32V480c0 17.7-14.3 32-32 32s-32-14.3-32-32V128c0-17.7 14.3-32 32-32zM352 224V480c0 17.7-14.3 32-32 32s-32-14.3-32-32V224c0-17.7 14.3-32 32-32s32 14.3 32 32zM192 288c17.7 0 32 14.3 32 32V480c0 17.7-14.3 32-32 32s-32-14.3-32-32V320c0-17.7 14.3-32 32-32zM96 416v64c0 17.7-14.3 32-32 32s-32-14.3-32-32V416c0-17.7 14.3-32 32-32s32 14.3 32 32z"/></svg>
                                        <p class="text-xs ml-2">Beginner</p>
                                    </div>
                                    <div class="flex items-center ml-2">
                                        <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M464 256A208 208 0 1 1 48 256a208 208 0 1 1 416 0zM0 256a256 256 0 1 0 512 0A256 256 0 1 0 0 256zM232 120V256c0 8 4 15.5 10.7 20l96 64c11 7.4 25.9 4.4 33.3-6.7s4.4-25.9-6.7-33.3L280 243.2V120c0-13.3-10.7-24-24-24s-24 10.7-24 24z"/></svg>
                                        <p class="text-xs ml-2">4 Month</p>
                                    </div>
                                </div>
                    
                                <div class="flex items-center">
                                <svg aria-hidden="true" class="w-4 h-4 text-black" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>First star</title><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                <svg aria-hidden="true" class="w-5 h-5 text-black" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Second star</title><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                <svg aria-hidden="true" class="w-5 h-5 text-black" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Third star</title><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                <svg aria-hidden="true" class="w-5 h-5 text-black" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Fourth star</title><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                <svg aria-hidden="true" class="w-5 h-5 text-gray-300 dark:text-gray-500" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Fifth star</title><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
                                <p class="text-xs ml-2">3866 reviews</p>
                            </div>
                        </div>
                    </div>
                    <div class="flex justify-center w-full">
                        <div class="flex flex-col w-11/12 py-6">
                            <h1 class="text-sm font-medium">Skill Covered</h1>
                            <p class="text-xs pt-2">Front-End Development Basics, HTML, CSS, Python syntax, Text Processing in Python, DevTools, Command Line Interface Basics, Code Debugging Basics Java Scripts</p>
                            <h1 class="text-sm font-medium pt-2">Prerequisites</h1>
                            <p class="text-xs pt-2">No Coding experience needed</p>
                        </div>
                    </div>
                </div>
            </div>

            
        </div>
    </section>
    
</template>

<script>

const selectedCities = ref();
const topics = ref([
    { name: 'Android', code: 'android' },
    { name: 'Web', code: 'web' },
    { name: 'Multiplatform', code: 'multiplatform' },
    { name: 'Cloud', code: 'cloud' },
    { name: 'Machine Learning', code: 'ML' }
]);

const cities = ref([
    { name: 'New York', code: 'NY' },
    { name: 'Rome', code: 'RM' },
    { name: 'London', code: 'LDN' },
    { name: 'Istanbul', code: 'IST' },
    { name: 'Paris', code: 'PRS' }
]);


</script>