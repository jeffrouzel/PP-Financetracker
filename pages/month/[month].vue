<template>
  <div>
    <h1>{{ month }}</h1>
    <CalendarTrack />
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
