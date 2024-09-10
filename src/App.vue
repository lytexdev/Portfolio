<template>
  <header>
    <Header />
  </header>

  <main>
    <About />

    <Contact />
  </main>
</template>

<script setup>
import Header from './components/Header.vue'
import About from './components/About.vue';
import Contact from './components/Contact.vue';
</script>

<style lang="scss">
@import './styles/app.scss';
</style>
