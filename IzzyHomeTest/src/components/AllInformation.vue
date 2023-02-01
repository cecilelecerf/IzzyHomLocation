<script>
import bdd from '../data.js'

export default {
  name:'AllInformation',
  components: {
  },
  data(){
    return{
        item : {
            type: Object,
            default: () => ({})
        },
        itemAdress: {
            type: Object,
            default:() => ({})
        }
    }
  },

  mounted(){

    bdd.forEach(e => {
        if(e['id']==this.$route.params.id){
            this.item = e;
            this.itemAdress = e['address'];
            return this.item;
        }
    });


  }
}
</script>

<template>
    <div class="container--flex">
        <h1>{{item['title']}}</h1>
        <p class="price">Loyer mensuel (charges comprises) : {{ item['full_rent_price'] }} €</p>
    </div>

    <figure>
        <img :src="item['main_picture']" alt="{{item['title']}}">
    </figure>

    <h2 v-if="item['type']==flat">Appartement à  {{itemAdress['city']}} ( {{itemAdress['postal_code']}} ) - <h2>test</h2></h2>
    <h2 v-else>Maison à {{itemAdress['city']}} ( {{itemAdress['postal_code']}} )</h2>


    <div class="container--flex">
        <p v-if="item['is_furnished']" >Meublé</p>
        <p v-else>Non-meublé</p>
        <p>Surface habitable : {{ item['living_area'] }}m²</p>
        <p>{{ item['rooms_count'] }} pièce(s)</p>
        <p>{{ item['bedrooms_count'] }} chambre(s)</p>
    </div>
</template>


<style lang="scss" scoped>
figure{
    height: 600px;
    margin: 50px 0;
    img{
        object-fit:cover;
    }

}
h2{
    margin: 20px 0;
    & + div{
        padding: 20px 20px;
        background-color: #3a4cbd;
    }
}
</style>