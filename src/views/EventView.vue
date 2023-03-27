<script setup>
import Navbar from "../components/Navbar.vue";
</script>

<template>
  <section class="relative bg-gray-900">
    <div class="z-10 relative">
      <Navbar/>
    </div>
    <div class="absolute inset-0 w-full h-full mix-blend-multiply">
      <img src="https://tech-enthusiast.herokuapp.com/img/carousel-1.20b9c62e.jpg" alt="JAKLITERA" class="absolute inset-0 object-cover object-center w-full h-full">
    </div>
  </section>
  <section class="bg-gray-50 mx-auto p-4 border-b">
    <form>
      <div class="flex items-center gap-12">
        <div>
          <ul class="grid gap-2 grid-cols-4">
            <li v-for="category in categories" :key="category.id">
              <input type="radio" :id="category.id" name="hosting" value="hosting-small" class="hidden peer" required>
              <label :for="category.id" class="text-sm inline-flex justify-between items-center py-3.5 px-6 w-full text-gray-500 bg-white rounded-lg border border-gray-200 cursor-pointer peer-checked:border-blue-600 peer-checked:text-blue-600 hover:text-gray-600 hover:bg-gray-100">
                <div class="w-full text-center text-base font-semibold">{{ category.name }}</div>
              </label>
            </li>
          </ul>
        </div>
        <div>or</div>
        <div class="flex-1">
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
    </form>
  </section>

  <section class="mt-10 mx-auto max-w-7xl sm:px-4">
    <div>
      <div class="mx-auto max-w-screen-sm text-center mb-10">
        <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">Explore Event</h2>
        <p class="font-light text-gray-500 lg:mb-16 sm:text-xl dark:text-gray-400">Excepteur sint occaecat cupidatat non proident.</p>
      </div>

      <div class="grid grid-cols-4 gap-6">
        <div v-for="index in 4" class="col-span-full lg:col-span-1 flex flex-col">
          <a href="#" class="block mb-6">
            <div class="relative shadow-md pb-1/1 overflow-hidden rounded-sm">
              <img
                  class="w-full h-80 object-cover object-center transform hover:scale-105 transition duration-700 ease-out"
                  src="/public/example-event.jpg"
                  alt="Event 01"
              />
            </div>
          </a>
          <div class="mb-3">
            <ul class="flex flex-wrap text-xs font-medium -m-1">
              <li class="m-1">
                <a class="inline-flex text-center text-gray-100 py-1 px-3 rounded-full bg-green-600 hover:bg-green-700 transition duration-150 ease-in-out"
                   href="#">Webinar</a>
              </li>
            </ul>
          </div>
          <h4 class="h4 mb-2">
            <a href="#" class="font-medium hover:text-green-700 transition duration-150 ease-in-out">The quick brown fox jumped over the lazy dog.</a>
          </h4>
          <div class="flex flex-wrap mt-2">
            <div class="flex items-center space-x-2 font-medium">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"/>
              </svg>
              <span class="font-light">Jan 17, 2020</span>
            </div>
          </div>
          <div class="flex flex-wrap mt-2">
            <div class="flex items-center space-x-2 font-medium">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
              </svg>
              <span class="font-light">10:00 AM - 12:00 PM</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      categories: [
        {
          id: 'category-java',
          name: 'Java'
        },
        {
          id: 'category-kotlin',
          name: 'Kotlin'
        },
        {
          id: 'category-flutter',
          name: 'Flutter'
        },
        {
          id: 'category-swift',
          name: 'Swift'
        }
      ]
    };
  },
}
</script>