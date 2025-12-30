<script setup>
import Tire from './Tire.vue';
const page = 'history';
</script>

<template>
    <div class="front-wheel">
        <span :id="page">FRONT-WHEEL</span><!--':'속성은 v-bind? 대체. 없으면 문자열로 page로 저장 ':'있으면 pagr안에 속성값인 'history'-->
        <Tire color= "BLUE" /><!--""안에는 변수,상수,속성 중 하나가 들어간다.-->
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