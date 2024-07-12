<template>
    <div class="flex w-screen h-[80px] text-green-950">
    
        <div class="w-[20%]">
            <div class="flex pl-5 items-center h-[100%] gap-4">
                <!-- IMAGE  -->
                <div class="flex text-2xl font-semibold">
                    <h1 class="text-yellow-400">Fin</h1>
                    <h1 class="text-green-600">Tracker</h1>
                </div>
            </div>
        </div>

        <div class="flex gap-12 w-[80%] items-center pl-10 shadow-bottom">
            <NuxtLink to="/home" class="hover:text-blue-500">Home</NuxtLink>
            <NuxtLink to="/contact" class="hover:text-blue-500">Contact</NuxtLink>
        </div>
    </div>
</template>