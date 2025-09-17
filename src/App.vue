<script setup>
  import SideBar from './components/SideBar.vue';
  import NavBar from './components/NavBar.vue';
</script>

<template>


<NavBar />


<div class="pt-16">
  <router-view></router-view>
</div>
<div>
  <side-bar/>
</div>

</template>
