<template>
  <main class="mt-5">
    <div class="container col-xxl-8 px-4">
      <Hero/>
    </div>

    <div class="container col-xxl-8 px-4">
      <About />
    </div>
<!-- 
    <div class="container col-xxl-8 px-4">
      <Projects />
    </div> -->


  </main>
</template>

<script>
import Hero from "../components/Hero.vue";
import About from "../components/About.vue";
import Projects from "../components/Projects.vue";  

export default {
  name: "HomeView",
  components: {
    Hero,
    About,
    Projects,
  }
};
</script>