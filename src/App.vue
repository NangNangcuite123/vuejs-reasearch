<template>
  <div id="app">
    <Navbar />
    <SignupForm />  
    <MyCard>
        <template #header>
          <img class="card-img w-100" src="https://images.unsplash.com/photo-1542640244-7e672d6cef4e?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="">
        </template>

        <p class="fs-3">Card Body</p>

        <template #footer>
          <button class="btn px-3 btn-danger">See More</button>
        </template>
    </MyCard>

  </div>
  
</template>


<script>
import SignupForm from './components/SignupForm.vue';
import Navbar from './components/Navbar.vue';
import Mybox from './components/Mybox.vue';
import MyCard from './components/Card.vue';
export default {
  name: 'app',
  components: {
    Navbar,
    SignupForm,
    Mybox,
    MyCard 
  }
}
</script>

