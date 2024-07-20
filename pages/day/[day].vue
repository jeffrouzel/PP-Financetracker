<template>
    <div>
    <!-- HEADER -->
        <div>
            <table class="w-full bg-white text-sm">
            <tr>
                <th><NuxtLink><div><ChChevronLeft class="size-6" /></div></NuxtLink></th>
                <th><div><h1> Day {{day}}</h1></div></th>
                <th><NuxtLink><div class="place-items-end"><ChChevronRight class="size-6 absolute" /></div></NuxtLink></th>
            </tr>
            </table>
        </div> 
        
        <AddExpense />
    </div>
</template>

<script setup lang="ts">
import { ref , watch } from 'vue';
import { useRoute } from 'vue-router';

import { ChChevronLeft, ChChevronRight} from '@kalimahapps/vue-icons';

const route = useRoute();
const day = ref(route.params.day);

watch(() => route.params.day, (newDay) => {
  day.value = newDay;
});
</script>