<template>
  <section class="relative bg-gray-900 min-h-screen">
    <div class="z-10 relative">
      <Navbar/>

      <div class="py-8 px-4 mx-auto max-w-screen-xl text-center lg:py-16 lg:px-12">
        <a href="#" class="inline-flex justify-between items-center py-1 px-1 pr-4 mb-7 text-sm text-gray-700 bg-gray-100 rounded-full dark:bg-gray-800 dark:text-white hover:bg-gray-200 dark:hover:bg-gray-700" role="alert">
          <span class="text-xs bg-green-600 rounded-full text-white px-4 py-1.5 mr-3">New</span> <span class="text-sm font-medium line-clamp-1">Bootcamp #1 Android Architecture Pattern</span>
          <svg class="ml-2 w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z" clip-rule="evenodd"></path></svg>
        </a>
        <h1 class="mt-0 lg:mt-8 mb-4 text-4xl font-extrabold tracking-tight leading-none text-white md:text-5xl lg:text-6xl dark:text-white">Android Enthusiast Jakarta</h1>
        <p class="mb-8 text-lg font-normal text-gray-500 lg:text-xl sm:px-16 xl:px-48 dark:text-gray-200">Develop high quality technology talent in 🇮🇩</p>
        <div class="flex flex-col mt-0 lg:mt-12 mb-8 lg:mb-24 space-y-4 sm:flex-row sm:justify-center sm:space-y-0 sm:space-x-4">
          <a href="#" class="inline-flex justify-center items-center py-3 px-5 text-base font-medium text-center text-white rounded-lg bg-green-700 hover:bg-green-800 focus:ring-4 focus:ring-green-300 focus:ring-gray-100">
            Join Our Community
            <svg class="ml-2 -mr-1 w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
          </a>
          <a href="#" class="inline-flex justify-center items-center py-3 px-5 text-base font-medium text-center text-white rounded-lg border border-gray-300 focus:ring-4 focus:ring-gray-100">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 -ml-1 w-5 h-5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6.75 3v2.25M17.25 3v2.25M3 18.75V7.5a2.25 2.25 0 012.25-2.25h13.5A2.25 2.25 0 0121 7.5v11.25m-18 0A2.25 2.25 0 005.25 21h13.5A2.25 2.25 0 0021 18.75m-18 0v-7.5A2.25 2.25 0 015.25 9h13.5A2.25 2.25 0 0121 11.25v7.5" />
            </svg>
            Explore FREE Events
          </a>
        </div>
        <div class="px-4 mx-auto text-center md:max-w-screen-md lg:max-w-screen-lg lg:px-36">
          <span class="font-semibold text-gray-400 uppercase">OUR PARTNER</span>
          <div class="flex flex-wrap justify-center items-center mt-8 text-gray-500 space-x-6 lg:space-x-20">
            <a href="#" class="mb-5 lg:mb-0 hover:text-gray-800 dark:hover:text-gray-400">
              <img src="/public/grab-logo.svg" class="w-20 lg:w-28" />
            </a>
            <a href="#" class="mb-5 lg:mb-0 hover:text-gray-800 dark:hover:text-gray-400 rounded px-2 py-1 bg-gray-200">
              <img src="/public/dicoding-logo.png" class="w-20 lg:w-32" />
            </a>
            <a href="#" class="mb-5 lg:mb-0 hover:text-gray-800 dark:hover:text-gray-400">
              <img src="/public/amartha-logo-2020.png" class="w-20 lg:w-36" />
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="absolute inset-0 w-full h-full mix-blend-multiply">
      <img src="https://tech-enthusiast.herokuapp.com/img/carousel-1.20b9c62e.jpg" alt="JAKLITERA" class="absolute inset-0 object-cover object-center w-full h-full">
    </div>
  </section>
</template>

<script>
import Navbar from "./Navbar.vue";

export default {
  components: {Navbar}
}
</script>