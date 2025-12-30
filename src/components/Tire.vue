<script setup>
//props: 부모 컨포넌트로부터 데이터를 전달받고 싶을 때 사용
const props = defineProps({
    color : String
});
</script>

<template>
    <div :style="{ color: props.color }">{{ props.color || 'BLACK' }} TIRE</div>    
</template>
<!--
style에 객체{}를 보내면 '{속성:속성값}'이 온다.

머스태시 문법 : 텍스트를 동적으로 출력하는 가장 대표적인 방법 중괄호 두개 {{ }}를 이용 
-->