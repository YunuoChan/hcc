<script setup>
import AdminLayout from '@/Layouts/AdminLayout.vue';
import { Head } from '@inertiajs/inertia-vue3';
import Sidebar from '@/Layouts/Sidebar.vue';
import Main from '@/Pages/Main.vue';
</script>

<template>
    <Head title="Dashboard" />

    <AdminLayout>
        <!-- Navigation template -->
        <template #navigation>
            <Nav></Nav> 
        </template>
        <!-- <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Dashboard
            </h2>
        </template> -->
        <template #main>
          <Main></Main>
        </template>
       
        <!-- <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-sm sm:rounded-lg">
                    <div class="p-6 bg-white border-b border-gray-200">
                        You're logged in!
                    </div>
                </div>
            </div>
        </div> -->
        <template #sidebar>
           <Sidebar></Sidebar> 
        </template>
    </AdminLayout>
</template>
