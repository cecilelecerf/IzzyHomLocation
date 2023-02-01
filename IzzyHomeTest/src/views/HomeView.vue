<script>
import RowCard from '../components/RowCard.vue';
import Search from '../components/Search.vue';
export default {
  name:'HomeView',
  components: {
    RowCard,
    Search,

  },
}
</script>

<template>
  <main>
    <Search/>
    <RowCard/>
  </main>
</template>
