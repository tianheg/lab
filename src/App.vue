<script setup>
import { RouterView } from 'vue-router'
import Sidebar from '@/components/Sidebar.vue'
</script>

<template>
  <header>
    <img
      alt="Site logo"
      class="logo"
      src="@/assets/logo.svg"
      width="125"
      height="125"
    />

    <div class="wrapper">
      <Sidebar msg="Hello Guys! Welcome to my Lab" />
    </div>
  </header>

  <RouterView />
</template>

<style>
@import '@/assets/base.css';

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;
  font-weight: normal;
}

header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

@media (min-width: 1024px) {
  body {
    place-items: center;
  }

  #app {
    display: flex;
    flex-wrap: wrap;
    position: relative;
    padding: 0 2rem;
  }

  header {
    flex-grow: 10;
    flex-basis: 300px;
    align-self: flex-start;
    position: sticky;
    --offset: 2rem;
    top: var(--offset);
  }

  main {
    flex-basis: 0;
    flex-grow: 999;
    min-width: 40%;
  }
}
</style>
