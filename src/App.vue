<template>
  <div id="app">
    <transition name="router-fade" mode="out-in">
      <keep-alive>
        <router-view v-if="$route.meta.keepAlive"></router-view>
      </keep-alive>
    </transition>
    <transition name="router-fade" mode="out-in">
      <keep-alive>
        <router-view v-if="!$route.meta.keepAlive"></router-view>
      </keep-alive>
    </transition> 
  </div>
</template>
<style>
  body {
    font-size: 16px;
    background-color: #f8f8f8;
    -webkit-font-smoothing: antialiased; /* 这个属性可以使页面上的字体抗锯齿,使用后字体看起来会更清晰 */
  }
</style>
