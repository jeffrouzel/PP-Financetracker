<script setup>
import { ref } from 'vue';

const users = ref([
    { id: 1, companyname: "Central Luzon College of Science and Technology" },
    { id: 2, companyname: "STI College" },
    { id: 3, companyname: "College of Maritime Leadership Innovation" },
    { id: 4, companyname: "PCI Tech Center Inc." },
    { id: 5, companyname: "Concentrix" },
    { id: 6, companyname: "HySeas III"},
    { id: 7, companyname: "Kongsberg" },
    { id: 8, companyname: "Maritime Merchant Marine Academy Graduate School" },
    { id: 9, companyname: "Hukbong Dagat Philippines" },
    { id: 10, companyname: "Inter-Global College Foundation Inc." },
    { id: 11, companyname: "Baliwag Maritime Academy" },
]);
</script>


<template>
    <div> Calendar </div>

    <div class="overflow-hidden rounded-lg border border-gray-200 shadow-md">
    <tr>
    
        <td><CalendarTrack /></td>
        <td><Inputmoney /></td>
    </tr>
    </div>
</template>
