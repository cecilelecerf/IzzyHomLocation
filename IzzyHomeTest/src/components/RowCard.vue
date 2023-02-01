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
            <RouterLink :to="/lease/+item.id" class="test">
                <Card :item="item" class="card"/>
            </RouterLink>
        </section>
    </div>
</template>

<style lang="scss" scoped>
    section{
        width: 35%;
        min-width: 300px;
        margin: 40px 40px;
        a{color: rgba(235,235,235,.64);}
        border: solid 1px #3a4cbd;
        &:hover{
            transition: color 0.5s, background-color 0.5s;
            background-color: #3a4cbd;
        }
    }
</style>
