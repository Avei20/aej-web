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