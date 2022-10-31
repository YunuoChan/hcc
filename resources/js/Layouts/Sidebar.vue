<script setup>
import { Link } from '@inertiajs/inertia-vue3';
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
</script>

<template>
    <div class="flex">
        <div class="flex flex-col h-screen p-3 bg-white shadow w-60">
            <div class="space-y-3">
                <div class="flex">
                    
                    <!-- Logo -->
                    <div class="shrink-0 flex items-center">
                        <Link :href="route('dashboard')">
                            <ApplicationLogo class="block h-9 w-auto" />
                        </Link>
                    </div>
                    <div class="flex items-center ml-3">
                        <h2 class="text-xl font-bold">Dashboard</h2>
                    </div>
                    <!-- Navigation Links -->
                    
                </div>
                <div class="flex-1">
                    <ul class="pt-2 pb-4 space-y-1 text-sm">
                        <Link :href="route('dashboard')">
                            <li class="rounded-sm flex items-cente p-2 space-x-3" :class="route().current() == 'dashboard' ? 'text-blue-500' : 'text-black'">
                                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 9v11a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V9"/><path d="M9 22V12h6v10M2 10.6L12 2l10 8.6"/></svg>

                                <span>Dashboard</span>
                             
                            </li>
                        </Link>
                        <Link>
                            <li class="rounded-sm flex items-cente p-2 space-x-3">
                                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path><circle cx="9" cy="7" r="4"></circle><path d="M23 21v-2a4 4 0 0 0-3-3.87"></path><path d="M16 3.13a4 4 0 0 1 0 7.75"></path></svg>
                                <span>Teacher</span>
                            </li>
                        </Link>
                      
                    </ul>
                </div>
            </div>
        </div>
        <!-- <div class="container mx-auto mt-12">
            <div class="grid grid-cols-1 gap-6 mb-6 lg:grid-cols-3">
                <div class="w-full px-4 py-5 bg-white rounded-lg shadow">
                    <div class="text-sm font-medium text-gray-500 truncate">
                        Total users
                    </div>
                    <div class="mt-1 text-3xl font-semibold text-gray-900">
                        12,00
                    </div>
                </div>
                <div class="w-full px-4 py-5 bg-white rounded-lg shadow">
                    <div class="text-sm font-medium text-gray-500 truncate">
                        Total Profit
                    </div>
                    <div class="mt-1 text-3xl font-semibold text-gray-900">
                        $ 450k
                    </div>
                </div>
                <div class="w-full px-4 py-5 bg-white rounded-lg shadow">
                    <div class="text-sm font-medium text-gray-500 truncate">
                        Total Orders
                    </div>
                    <div class="mt-1 text-3xl font-semibold text-gray-900">
                        20k
                    </div>
                </div>
            </div>
        </div> -->
    </div>
</template>