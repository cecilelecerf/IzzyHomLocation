<script>
import bdd from '../data.js';
export default {
    setup(){
        console.log(bdd);
    },
    data(){
        return {
            bdd,
        }
    }
}
</script>


<template>
  <section>
    <figure>
        <img :src="bdd[0]['main_picture']" alt="">
    </figure>
    <div class="container--flex">
        <div class="items--left">
            <p>{{bdd[0]['title']}}</p>
            <p>{{bdd[0]['living_area'] }} m²</p>
        </div>
        <div class="items--right">
            <p>{{ bdd[0]['full_rent_price'] }} €</p>
        </div>
        
    </div>
  </section>
</template>

<style lang="scss" scoped>
    section {
        width: 35%;
    }
    img{
        width: 100%;
    }

</style>