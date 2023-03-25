<script>
import HeaderComponentVue from './components/HeaderComponent.vue';

export default {
  components: {
    HeaderComponentVue,
  }
}
</script>

<template>
  <section id="app">
      <HeaderComponentVue />
      <router-view></router-view>
  </section>
</template>

<style>
* {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  text-decoration: none;
}

#app {
  width: 100%;
  height: 100%;
  margin: 0 auto;
  background: rgb(39, 39, 39);
}

@import url('https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;0,1000;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900;1,1000&display=swap');
</style>
