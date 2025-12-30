<script setup>
import { computed, reactive } from 'vue';

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
    console.log('call getMvpName')
    return state.players.find(item => item.id === state.mvpId)?.name || 없음;
}

const computedMvpName = computed( () => {
    console.log('call computedMvpName');
    return state.players.find(item => item.id === state.mvpId)?.name || '없음';
} );
const increaseMvpId= () => state.mvpId++;
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
        <!--함수는 호출할 때마다 함수 안의 코드가 실행이 된다.-->
        <div>{{ getMvpName() }}</div>
        <div>{{ getMvpName() }}</div>
        <div>{{ getMvpName() }}</div>
        <hr>
        <!--컴퓨티드는 보낸 콜백함수가 딱 한번만 실행이 되고 결과가 return이 된다.-->
        <div>{{ computedMvpName }}</div>
        <div>{{ computedMvpName }}</div>
        <div>{{ computedMvpName }}</div>
    </div>
    <div>{{state.mvpId}}</div>
    <!--미니 미션, 버튼을 클릭하면 mvpId가 1씩 올라가게 해주세요. -->
    <button @click="increaseMvpId">mvpId 증가</button>
    
</div>

</template>

<style scoped>

</style>