<template>
 <Navbar></Navbar>
 <router-view></router-view>
 <Footer class="w-full"></Footer>
</template>
<script>
import Popular from './components/Popular.vue';
import Navbar from './components/Navbar.vue';
import HomeView from './views/HomeView.vue';
import Footer from './components/footer.vue';
export default{
  components: {
    HomeView,
    Navbar,
    Popular,
    Footer,
  }
}
</script>