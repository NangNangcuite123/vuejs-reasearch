<template>
    <header  :class="{ 'scrolled': isScrolled }"  class="fixed-top w-100 transition">
      <nav class="navbar navbar-expand-lg py-3">
  <div class="container d-flex align-item-center ">
    <a class="navbar-brand p-0" href="#">
      <span class="cafe">Cafe</span>
      <span class="street">Street</span>
    </a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavDropdown">
      <ul class="navbar-nav m-auto">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Menu
          </a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
          </ul>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">About us</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Contact</a>
        </li>
      </ul>
      <div class="ms-auto">
        <a href="#" class="link-login text-decoration-none px-3 py-2 rounded-1 text-light text-center d-block">
          Login
        </a>
      </div>
    </div>
  </div>
    </nav>
    </header>
</template>
<script>
export default {
  data() {
    return {
      isScrolled: false
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.isScrolled = window.scrollY > 50; // show background after 50px
    }
  }
};
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    line-height: 1.6;

  }
  
  body{
    font-family: "Poppins", sans-serif;
  }
  header.scrolled {
  background-color: #F6EBDA;
  transition: background-color 0.2s ease-in-out;
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
}
  .cafe{
    font-size: 1.6rem;
    display: inline-block;
    color: #F4AE26;
  }
  .street{
    font-size: 1.6rem;
    display: inline-block;
    color: #2F2105;
    margin-left:8px;
  }
  .nav-link{
    font-size: 18px;
    color: #000000;
    font-weight: 400;
    padding: 0px 15px !important;
  }
  .nav-link.active{
    color: #F4AE26 !important;
  }
  .link-login{
    background-color: #2F2105;
  }
</style>