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
                <NuxtLink :to="'/day/' + day.date.getDate()" class="hover:text-blue-500">
                  <th class="day-number">{{ day.date.getDate() }}</th>
                </NuxtLink>
                <td class="text-green-600">{{ day.currency }}</td>       
            </tr>
        </tbody>
    </table>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

// Function to generate random currency values
const generateRandomCurrency = () => {
  return `$${(Math.random() * 300).toFixed(2)}`;
};

// Function to generate days for the current month
const generateDaysForMonth = (year: number, month: number) => {
  const days = [];
  const date = new Date(year, month, 1);
  while (date.getMonth() === month) {
    days.push({
      date: new Date(date),
      currency: generateRandomCurrency(),
    });
    date.setDate(date.getDate() + 1);
  }
  return days;
};

// Current year and month
const getMonthName = (month: number) => {
  const months = [
    "January",
    "February",
    "March",
    "April",
    "May",
    "June",
    "July",
    "August",
    "September",
    "October",
    "November",
    "December",
  ];
  return months[month];
};

const currentYear = 2024;
const currentMonth = 1; // To be integrated to the month pages

// Generate days for the current month
const days = ref(generateDaysForMonth(currentYear, currentMonth));
</script>
