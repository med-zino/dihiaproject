<template>
 <NavbarVue />
  <img :src="logoImage" alt="DM Logo" class="logo-image" data-aos="fade-up">
   <ImagesContainerVue />

</template>

<script>
import ImagesContainerVue from './components/ImagesContainer.vue'
import NavbarVue from './components/Navbar.vue'
import AOS from 'aos';
import 'aos/dist/aos.css';

  
export default {
  name: 'App',
  components: {
    NavbarVue,
    ImagesContainerVue

  },
   data() {
    return {
 logoImage: require('../public/cover.png'), 
    }
} , 
 mounted() {
    AOS.init({
      delay: 200, 
      duration: 2000,
       easing: 'ease',
    });
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  }
  img {
  width: 90%;
  height: 600px;
  margin-bottom: 100px;
  }
</style>
