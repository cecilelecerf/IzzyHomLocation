<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo (2).png" width="125" height="125" />

    <div class="wrapper">
      <nav>
        <RouterLink to="/">Accueil</RouterLink>
        <RouterLink to="/about">A propos</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style lang="scss" scoped>
header{
  margin : 0 calc(50% - 62.5px) ;
  width: fit-content;
  nav {
    display: flex;
    justify-content: space-around;
  }
}

</style>
