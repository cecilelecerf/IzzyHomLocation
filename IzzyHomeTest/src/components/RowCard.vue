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
  mounted(){
    
    if(this.$route.query.is_furnished=='furnished'){
        this.bdd.forEach(e => {
            if(e.is_furnished ==false){
                this.bdd.splice(this.bdd.indexOf(e), 1)
            }   
        });
    }
    // console.log(this.$route.query.is_furnised);
    if(this.$route.query.is_furnised=='not_furnished'){
        // console.log('ok')
        this.bdd.forEach(e => {
            if(e.is_furnished ==true){
                this.bdd.splice(this.bdd.indexOf(e), 1)
            }   
        });
    }
    if(this.$route.query.min_living_area){
        this.bdd.forEach(e => {
            if(e.living_area < this.$route.query.min_living_area){
                this.bdd.splice(this.bdd.indexOf(e), 1)
            }   
        });
    }
    if(this.$route.query.max_living_area){
        this.bdd.forEach(e => {
            if(e.living_area > this.$route.query.max_living_area){
                this.bdd.splice(this.bdd.indexOf(e), 1)
            }   
        });
    }
    if(this.$route.query.min_full_rent_price){
        this.bdd.forEach(e => {
            if(e.full_rent_price < this.$route.query.min_full_rent_price){
                this.bdd.splice(this.bdd.indexOf(e), 1)
            }   
        });
    }
    if(this.$route.query.max_full_rent_price){
        this.bdd.forEach(e => {
            if(e.full_rent_price > this.$route.query.max_full_rent_price){
                this.bdd.splice(this.bdd.indexOf(e), 1)
            }   
        });
    }
    console.log(this.bdd.length);
    console.log(this.$route.query);
  }
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
