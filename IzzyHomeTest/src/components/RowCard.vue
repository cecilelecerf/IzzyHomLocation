<script>
import Card from '../components/Card.vue';
import bdd from '../data.js'
export default {
  name:'RowCard',
  components: {
    Card,
  },
  data(){
    return {
        bdd,
    }
  },
}
</script>

<template>
    <div class="container--flex row">
        <section v-for="item in bdd" :key="item.id">
            <Card :item="item"/>
        </section>
    </div>
</template>

<style lang="scss" scoped>
    section {
        width: 35%;
        min-width: 300px;
    }
</style>
