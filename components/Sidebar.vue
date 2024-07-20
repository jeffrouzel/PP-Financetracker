<template>
  <div class="flex flex-col w-[250px] h-screen border-r-2 text-xs font-semibold text-gray-500 items-left pl-4">
    <div class="flex flex-col items-center gap-2 pb-6">
      <h1>Jeff Rouzel Bat-og</h1>
      <h1>Super Admin</h1>
    </div>

    <tr v-for="month in months" :key="month.id" >
        <div class="flex items-center gap-2 hover:text-blue-500 h-10">
          <NuxtLink :to="'/month/'+ month.month">
            <div>{{month.month}}</div>
          </NuxtLink>
        </div>
    </tr>
    
    
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const months = ref([
    { id: 1, month: "January" },
    { id: 2, month: "February" },
    { id: 3, month: "March" },
    { id: 4, month: "April" },
    { id: 5, month: "May" },
    { id: 6, month: "June" },
    { id: 7, month: "July" },
    { id: 8, month: "August" },
    { id: 9, month: "September" },
    { id: 10, month: "October" },
    { id: 11, month: "November" },
    { id: 12, month: "December" },
]);
</script>
