<script setup>
let loading = false;

const fruits = [ 'apple', 'banana', 'pear'];
</script>

<template>
    <h3>Page103</h3>
    <!-- v-if 디렉티브 -->
    <template v-if="loading">로딩 중</template>
    <!--template 텍스트로 변환시 사용-->
    <div v-else>로딩 완료</div>
    <!--위랑 같은 의미-->
    <div>{{ loading ? '로딩 중' : '로딩 완료' }}</div>

    <hr>

    <div v-show="loading">show 로딩 중</div>
    <div v-show="!loading">show 로딩 완료</div>
    <hr>
    <!-- v-for 사용할 때 주의사항이 있다. 항상 key속성을 주셔야 하며 유일값이어야 한다.-->
    <div v-for="(item, idx) in fruits" :key="idx">{{idx+1}}. {{item}}</div>

</template>

<style scoped>

</style>