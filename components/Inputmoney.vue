<script setup>
import { ref } from 'vue';

const allowance = ref([
  { moneyID: 1, name: "Food", amount: 700},
  { moneyID: 2, name: "Transportation", amount: 200}, 
  { moneyID: 3, name: "Bills", amount: 1500}, 
  { moneyID: 4, name: "Savings", amount: 100}, 

]);

</script>

<template>
  <div class="w-56 h-56 overflow-hidden rounded-lg border border-gray-200 shadow-md">
      <table class="w-full border-collapse bg-white text-center text-sm text-gray-500">
          <thead class="bg-gray-50">
              <tr>
                <th scope="col" class="px-6 py-4 font-normal text-gray-900">Allowance Type</th>
                <th scope="col" class="px-6 py-4 font-normal text-gray-900">Amount Remaining</th>
              </tr>
          </thead>

          <tbody>
              <tr v-for="money in allowance" class="hover:bg-gray-50">
                  <th class="day-number">{{ money.name }}</th>
                  <td class="text-green-600">{{ money.amount }}</td>       
              </tr>
          </tbody>
      </table>
  </div>


</template>