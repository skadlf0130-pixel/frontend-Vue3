<script setup>
import { reactive } from 'vue';

const state = reactive({
    mvpId: 7,
    players: [
        {id: 7, name: 'John Doe'},
        {id: 9, name: 'Jene Lee'},
        {id: 12, name: 'James Park'},
    ]
});

const getMvpName= () => {
    //if(state.mvpId){
    //    const player= state.players.find(item => item.id === state.mvpId);
    //    if(player){
    //        return player.name;
    //    }
    //}
    //return'없음';
    console.log('call getMvpName');
    return state.players.find(item => item.id === state.mvpId)?.name || 없음;
}
</script>

<template>
<h3>Page118.vue</h3>
<div>
    <h1>오늘의 MVP</h1>
    <div>
        <!--'.' 있으면 리턴메서드 객체의 주소값이 넘어온걸 알수있다.
        
        ()안에 있는 건 함수주소값
        
        ?(옵셔널 체이닝)는 앞의 값이 undefined 또는 null이면 에러를 내지 않고 그냥 undefined를 반환-->
        <template v-if = "state.mvpId"> {{ state.players.find(m => m.id === state.mvpId)?.name || 없음 }}</template>
        <template v-else>없음</template>
        <hr>
        <div>{{ getMvpName() }}</div>
    </div>
</div>

</template>

<style scoped>

</style>