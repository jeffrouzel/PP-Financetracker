<template>
  <div class="p-4">
    <form @submit.prevent="addExpense" class="mb-4 flex gap-4">
      <input v-model="newExpense.id" placeholder="ID" class="border p-2" required />
      <input v-model="newExpense.amount" type="number" placeholder="Amount" class="border p-2" required />
      <select v-model="newExpense.moneytype" class="border p-2" required>
        <option disabled value="">Select Money Type</option>
        <option value="Food">Food</option>
        <option value="Transportation">Transportation</option>
        <option value="Bills">Bills</option>
        <option value="Savings">Savings</option>
      </select>
      <button type="submit" class="bg-blue-500 text-white p-2 rounded">Add</button>
    </form>
    
    <div class="grid grid-cols-5 gap-4">
      <div v-for="expense in expenses" :key="expense.id" class="border p-4 rounded bg-gray-100">
        <p><strong>ID:</strong> {{ expense.id }}</p>
        <p><strong>Amount:</strong> {{ expense.amount }}</p>
        <p><strong>Money Type:</strong> {{ expense.moneytype }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const newExpense = ref({
  id: '',
  amount: '',
  moneytype: ''
})

const expenses = ref([])

const addExpense = () => {
  expenses.value.push({ ...newExpense.value })
  newExpense.value.id = ''
  newExpense.value.amount = ''
  newExpense.value.moneytype = ''
}
</script>

<style scoped>
form input {
  flex: 1;
}
</style>
