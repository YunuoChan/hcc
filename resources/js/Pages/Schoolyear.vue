<script setup>

import { Head } from '@inertiajs/inertia-vue3';

    const props = defineProps({
            schoolyears: Object
        });
</script>


<template>
    <Head title="Select School Year" />

    <!-- BG  -->
    <div class="school-year-bg "></div>
    <div class="overlay">
        <div class="schoolyear-data flex">
            <div  v-for="schoolyears in props.schoolyears" :key="schoolyears.id" class="w-full max-w-sm bg-gradient-to-t from-sky-300 to-blue-900 rounded-lg border border-gray-200 shadow-md dark:bg-gray-800  min-wid-15-rem mx-3">
                <div class="flex justify-end px-4 pt-4">
                    <button id="dropdownButton" data-dropdown-toggle="dropdown" class="inline-block text-gray-500 dark:text-gray-400 rounded-lg text-sm p-1.5" type="button">
                        <svg xmlns="http://www.w3.org/2000/svg" class="dark:hover:stroke-red-500" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#ffffff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="3 6 5 6 21 6"></polyline><path d="M19 6v14a2 2 0 0 1-2 2H7a2 2 0 0 1-2-2V6m3 0V4a2 2 0 0 1 2-2h4a2 2 0 0 1 2 2v2"></path><line x1="10" y1="11" x2="10" y2="17"></line><line x1="14" y1="11" x2="14" y2="17"></line></svg>                    
                    </button>
                </div>
                <div class="flex flex-col items-center pb-10">
                    <img class="mb-3 w-24 h-24 rounded-full shadow-lg" src="assets/img/logo.jpg" alt="Bonnie image">
                    <h5 class="mb-1 text-xl font-medium text-gray-900 dark:text-white">S.Y. {{ schoolyears.sy_from }} - {{schoolyears.sy_to}}</h5>
                    <span class="text-sm text-gray-200 dark:text-gray-200">Created on {{ schoolyears.created_at }}</span>
                    <div class="flex mt-4 space-x-3 md:mt-6">
                        <a href="#" class="inline-flex items-center py-2 px-4 text-sm font-medium text-center text-white bg-blue-700 rounded-lg justify-center hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-transparent w-36">Select</a>
                    </div>
                </div>
            </div>
           

            <!-- NEW RECORD -->
            <div class="w-full max-w-sm bg-white rounded-lg border border-gray-200 shadow-md dark:bg-gray-800 dark:border-gray-700 min-wid-15-rem mx-3">
                <div class="flex justify-end px-4 pt-4 w-6 h-11">
                </div>
                <div class="flex flex-col items-center pb-10 px-4 pt-4">
                    <img class="mb-3 w-24 h-24 rounded-full shadow-lg" src="assets/img/logo.jpg" alt="Bonnie image">
                    <span class="text-sm text-gray-500 dark:text-gray-400">Add new Record</span>
                    <div class="flex mt-4 space-x-3 md:mt-6">
                        <a href="#" class="inline-flex items-center py-2 px-4 text-sm font-medium text-center justify-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-transparent w-36">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#11ff6c" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="12" y1="5" x2="12" y2="19"></line><line x1="5" y1="12" x2="19" y2="12"></line></svg>
                            <span>Add</span> 
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
