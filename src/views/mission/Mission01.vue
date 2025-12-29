<script setup>
let loading= true;

const students = [
    { name: '수영', present: true },
    { name: '준하', present: false },
    { name: '가은', present: true },
    { name: '수빈', present: true },
    { name: '예림', present: false }
];
</script>

<template>
    <h3>Mission01.vue</h3>

    <div v-for="(item, idx) in students" :key="idx">{{item.name}} {{item.present ? '출석' :''}}
    <span v-if="item.present">출석</span>
    <span v-show="item.present">출석</span>
    <!--3가지 방법-->
    </div> 


</template>

<style scoped>

</style>