<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <Drawer class="header"/>
    <transition name="component-fade" mode="out-in">
      <router-view class="main"/>
    </transition>
    <bottom-bar class="footer"/>
  </div>
</template>

<script>
import Drawer from '@/components/Drawer'
import BottomBar from '@/components/BottomBar'
export default {
  name: 'App',
  components:{
    Drawer,
    BottomBar
  }
}
</script>


<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding-top: 0px;
  overflow: hidden;
}

.main{
  margin-top: 55px;
  margin-bottom: 50px;
}
.component-fade-enter-active, .component-fade-leave-active {
  transition: opacity .2s ease;
}
.component-fade-enter, .component-fade-leave-to {
  opacity: 0;
}

</style>
