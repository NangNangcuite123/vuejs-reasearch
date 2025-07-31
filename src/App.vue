<template>
    <Navbar />
    <!-- <SignupForm />   -->
    <Banner />

</template>

<script>
// import SignupForm from './components/SignupForm.vue';
import Navbar from './components/Navbar.vue';
// import MyCard from './components/Card.vue';
import Banner from './components/Banner.vue';
export default {
  name: 'app',
  components: {
    Navbar,
    Banner
  }
}
</script>

