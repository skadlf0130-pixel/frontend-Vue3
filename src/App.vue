<script setup>
import { globalState } from './globalstate';
</script>

<template>
  <div>
    <nav>
      <router-link v-for="item in globalState" :to="`/${item}`" :key="item">{{item}}</router-link>

      <!--
      <router-link to= "/component">컴포넌트</router-link>
      <router-link to= "/page98">Page98</router-link>
      <router-link to= "/page103">Page103</router-link>
      <router-link to= "/mission01">Mission01</router-link>
      <router-link to= "/page108">Page108</router-link>
      <router-link to= "/page110">Page110</router-link>
      -->
    </nav>
    <main>
      <router-view />
    </main>
  </div>
</template>

<style scoped>
nav > a {display: inline-block;}

</style>