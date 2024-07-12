<script setup>
import { ref } from 'vue';

const days = ref([
  { date: new Date(2024, 6, 1), currency: '$100' },
  { date: new Date(2024, 6, 2), currency: '$200' },
  { date: new Date(2024, 6, 3), currency: '$100' },
  { date: new Date(2024, 6, 4), currency: '$200' },
  { date: new Date(2024, 6, 5), currency: '$100' },
  { date: new Date(2024, 6, 6), currency: '$200' },
  { date: new Date(2024, 6, 7), currency: '$100' },
  { date: new Date(2024, 6, 8), currency: '$200' },
  { date: new Date(2024, 6, 9), currency: '$100' },
  { date: new Date(2024, 6, 10), currency: '$200' },
  { date: new Date(2024, 6, 11), currency: '$100' },
  { date: new Date(2024, 6, 12), currency: '$200' },
  { date: new Date(2024, 6, 13), currency: '$100' },
  { date: new Date(2024, 6, 14), currency: '$200' },
  { date: new Date(2024, 6, 15), currency: '$100' },
  { date: new Date(2024, 6, 16), currency: '$200' },
  { date: new Date(2024, 6, 17), currency: '$100' },
  { date: new Date(2024, 6, 18), currency: '$200' },
  { date: new Date(2024, 6, 19), currency: '$100' },
  { date: new Date(2024, 6, 20), currency: '$200' },
  { date: new Date(2024, 6, 21), currency: '$100' },
  { date: new Date(2024, 6, 22), currency: '$200' },
  { date: new Date(2024, 6, 23), currency: '$100' },
  { date: new Date(2024, 6, 24), currency: '$200' },
  { date: new Date(2024, 6, 25), currency: '$100' },
  { date: new Date(2024, 6, 26), currency: '$200' },
  { date: new Date(2024, 6, 27), currency: '$100' },
  { date: new Date(2024, 6, 28), currency: '$200' },
  { date: new Date(2024, 6, 29), currency: '$100' },
  { date: new Date(2024, 6, 30), currency: '$200' },
  { date: new Date(2024, 6, 31), currency: '$100' },

]);

</script>

<template>
  <div class="overflow-hidden rounded-lg border border-gray-200 shadow-md">
    <table class="w-full border-collapse bg-white text-center text-sm text-gray-500">
        <thead class="bg-gray-50">
            <tr>
              <th scope="col" class="px-6 py-4 font-medium text-gray-900">Day</th>
              <th scope="col" class="px-6 py-4 font-medium text-gray-900">Expense</th>
            </tr>
        </thead>

        <tbody>
            <tr v-for="day in days" :key="day.date" class="hover:bg-gray-50">
                <NuxtLink :to="'/user/' + day.date" class="hover:text-blue-500">
                  <th class="day-number">{{ day.date.getDate() }}</th>
                </NuxtLink>
                <td class="text-green-600">{{ day.currency }}</td>       
            </tr>
        </tbody>
    </table>
  </div>
</template>
