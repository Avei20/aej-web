<template>

    <section class="relative bg-gray-900">
        <Navbar />
    </section>

    <section class="relative bg-gray-900 w-full rounded-bl-[95px] max-sm:h-96 max-sm:rounded-none">
        <div class="flex flex-row w-full items-center max-sm:flex-col">
            <div class="w-1/2 flex flex-col text-white p-16 max-sm:w-full">
                <h1 class="text-4xl font-medium">Individual Learners Catalog</h1>
                <p>Transform your career with Nanodegree programs starting at <span class="font-bold">$399/mo.</span></p>
            </div>
            <div class="flex-1 w-1/ mr-20 max-sm:w-11/12 max-sm:mr-0 ">
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
                <ul class="grid gap-2 grid-cols-6 max-sm:grid-cols-1">
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
        <div class="w-11/12 grid gap-5 grid-cols-2 max-lg:grid-cols-1">
            <div class="flex flex-row max-sm:flex-col drop-shadow-2xl bg-gray-50" v-for="catalogue in catalogueList" :key="catalogue.id">
                <div class="border-r-2 p-3 w-60 max-sm:w-full">
                    <div class="w-full">
                        <img src="/public/aej-logo.svg" class="w-36 max-md:w-full max-md:h-[120px] bg-green-700  rounded-bl-[55px] h-[130px]" alt="AEJ Logo"/>
                    </div>
                    <div class="flex flex-col sm:flex-col justify-center items-center mt-3 max-sm:flex-row">
                        <a href="#" class="flex flex-row py-3 px-5 mb-2 max-sm:mb-0 max-sm:mr-2 justify-between  items-center w-fit text-sm font-medium text-center text-white rounded-lg bg-green-700 hover:bg-green-800 focus:ring-4">
                            Program Details
                        </a>
                        <a href="#" class="flex w-fit justify-center  items-center py-3 px-2 text-sm font-medium text-center text-green-700 rounded-lg border border-green-700 focus:ring-4 focus:ring-gray-100">
                            Download Syllabus
                        </a>
                    </div>
                </div>
                <div class="flex flex-col w-full items-center">
                    <div class="flex flex-col w-full items-center py-6">
                        <div class="flex flex-col w-11/12">
                            <div>
                                <button class="bg-lime-400 px-4 py-2 mr-2 rounded-full text-xs w-28" v-for="tag in catalogue.tags">{{ tag }}</button>
                            </div>
                            <h1 class="text-xl font-semibold pt-4">{{ catalogue.name }}</h1>
                            <p class="text-xs pt-2">{{ catalogue.desc }}</p>
                        </div>
                    </div>
                    <div class="w-full bg-gray-200 flex justify-center mt-8">
                        <div class="flex flex-row justify-between w-11/12 py-4">
                                <div class="flex items-center">
                                    <div class="flex items-center">
                                        <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 640 512"><!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M576 0c17.7 0 32 14.3 32 32V480c0 17.7-14.3 32-32 32s-32-14.3-32-32V32c0-17.7 14.3-32 32-32zM448 96c17.7 0 32 14.3 32 32V480c0 17.7-14.3 32-32 32s-32-14.3-32-32V128c0-17.7 14.3-32 32-32zM352 224V480c0 17.7-14.3 32-32 32s-32-14.3-32-32V224c0-17.7 14.3-32 32-32s32 14.3 32 32zM192 288c17.7 0 32 14.3 32 32V480c0 17.7-14.3 32-32 32s-32-14.3-32-32V320c0-17.7 14.3-32 32-32zM96 416v64c0 17.7-14.3 32-32 32s-32-14.3-32-32V416c0-17.7 14.3-32 32-32s32 14.3 32 32z"/></svg>
                                        <p class="text-xs ml-2">{{ catalogue.level }}</p>
                                    </div>
                                    <div class="flex items-center ml-2">
                                        <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M464 256A208 208 0 1 1 48 256a208 208 0 1 1 416 0zM0 256a256 256 0 1 0 512 0A256 256 0 1 0 0 256zM232 120V256c0 8 4 15.5 10.7 20l96 64c11 7.4 25.9 4.4 33.3-6.7s4.4-25.9-6.7-33.3L280 243.2V120c0-13.3-10.7-24-24-24s-24 10.7-24 24z"/></svg>
                                        <p class="text-xs ml-2">{{ catalogue.duration > 1 ? `${catalogue.duration} months.` : `${catalogue.duration} month` }}</p>
                                    </div>
                                </div>
                    
                                <div class="flex items-center">
                                <Rating v-model="value" readonly  :cancel="false"/>

                                <p class="text-xs ml-2">{{ catalogue.totalReview > 1 ? `${catalogue.totalReview} reviews` : `${catalogue.totalReview} review`  }}</p>
                            </div>
                        </div>
                    </div>
                    <div class="flex justify-center w-full">
                        <div class="flex flex-col w-11/12 py-6">
                            <h1 class="text-sm font-medium">Skill Covered</h1>
                            <p class="text-xs pt-2">
                                <span v-for="skill in catalogue.skillsCovered ">{{ skill == catalogue.skillsCovered[catalogue.skillsCovered.length - 2] ? `${skill}, ` : `${skill}.` }} </span>
                            </p>
                            <h1 class="text-sm font-medium pt-2">Prerequisites</h1>
                            <p class="text-xs pt-2">{{ catalogue.prerequites == "" ? 'No Coding experience needed.' : catalogue.prerequites }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <NavFooter />
    
</template>

<script setup>

import NavFooter from "../components/NavFooter.vue";
import Navbar from "../components/Navbar.vue";
import { ref } from "vue";

const catalogueList = ref([
    {
        id: 1,
        name: 'Introduction to Programming Beginner',
        tags: ['Nanodegree', 'Double'],
        desc: 'A first step for beginers towards careers in web and app development, machine learning, data science, AI and More.',
        level: 'Beginner',
        duration: '4',
        totalReview: 3866,
        skillsCovered: ['Front-End Development Basics', 'HTML', 'CSS', 'Python syntax', 'Text Processing in Python', 'DevTools', 'Command Line Interface Basics', 'Code Debugging', 'Basics Java Script'],
        prerequites: '',
    },
    {
        id: 2,
        name: 'Introduction to Programming C#',
        tags: ['Nanodegree'],
        desc: 'oeatnuasoeuh antsoehuanteohu oatensuh aoetuaoetnuhaoe ustaoehu a',
        level: 'Beginner',
        duration: '4',
        totalReview: 3866,
        skillsCovered: ['Front-End Development Basics', 'HTML', 'CSS', 'Python syntax', 'Text Processing in Python', 'DevTools', 'Command Line Interface Basics', 'Code Debugging Basics Java Script'],
        prerequites: '',
    },
    {
        id: 3,
        name: 'Introduction to Programming C#',
        tags: ['Nanodegree'],
        desc: 'oeatnuasoeuh antsoehuanteohu oatensuh aoetuaoetnuhaoe ustaoehu a',
        level: 'Beginner',
        duration: '4',
        totalReview: 3866,
        skillsCovered: ['Front-End Development Basics', 'HTML', 'CSS', 'Python syntax', 'Text Processing in Python', 'DevTools', 'Command Line Interface Basics', 'Code Debugging Basics Java Script'],
        prerequites: '',
    },
    {
        id: 4,
        name: 'Introduction to Programming C#',
        tags: ['Nanodegree'],
        desc: 'oeatnuasoeuh antsoehuanteohu oatensuh aoetuaoetnuhaoe ustaoehu a',
        level: 'Beginner',
        duration: '4',
        totalReview: 3866,
        skillsCovered: ['Front-End Development Basics', 'HTML', 'CSS', 'Python syntax', 'Text Processing in Python', 'DevTools', 'Command Line Interface Basics', 'Code Debugging Basics Java Script'],
        prerequites: '',
    },
    {
        id: 5,
        name: 'Introduction to Programming C#',
        tags: ['Nanodegree'],
        desc: 'oeatnuasoeuh antsoehuanteohu oatensuh aoetuaoetnuhaoe ustaoehu a',
        level: 'Beginner',
        duration: '4',
        totalReview: 3866,
        skillsCovered: ['Front-End Development Basics', 'HTML', 'CSS', 'Python syntax', 'Text Processing in Python', 'DevTools', 'Command Line Interface Basics', 'Code Debugging Basics Java Script'],
        prerequites: '',
    },
    {
        id: 6,
        name: 'Introduction to Programming C#',
        tags: ['Nanodegree'],
        desc: 'oeatnuasoeuh antsoehuanteohu oatensuh aoetuaoetnuhaoe ustaoehu a',
        level: 'Beginner',
        duration: '4',
        totalReview: 3866,
        skillsCovered: ['Front-End Development Basics', 'HTML', 'CSS', 'Python syntax', 'Text Processing in Python', 'DevTools', 'Command Line Interface Basics', 'Code Debugging Basics Java Script'],
        prerequites: '',
    },
])

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

const value = ref(2);


</script>