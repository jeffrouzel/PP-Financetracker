<template>
  <div>
    <h1>{{ month }}</h1>
    <!-- Add the calendar and other functionalities here -->
  </div>
</template>

<script setup lang="ts">
import { ref , watch } from 'vue';
import { useRoute } from 'vue-router';

const route = useRoute();
const month = ref(route.params.month);

watch(() => route.params.month, (newMonth) => {
  month.value = newMonth;
});
</script>
