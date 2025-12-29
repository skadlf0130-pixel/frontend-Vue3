<script setup>
import Tire from './Tire.vue';
const page = 'history';
</script>

<template>
    <div class="front-wheel">
        <span :id="page">FRONT-WHEEL</span>
        <Tire color= "BLUE" />
    </div>
</template>

<style scoped>
#history { text-decoration: underline; }
.front-wheel{
    border: 1px solid black;
    border-radius: 50%;
    display: flex;  /*자식을 컨트롤 하기 위해서 flex를 사용*/
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 150px;
    height:150px;
}
</style>