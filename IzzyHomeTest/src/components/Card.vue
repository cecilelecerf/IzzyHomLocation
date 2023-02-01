<script>
export default {
    props: {
        item : {
            type: Object,
            default: () => ({})
        }
    },
}
</script>


<template>
    <figure>
        <img :src="item['main_picture']" :alt="item['title']">
        <img src="../assets/Rectangle 1.png" alt="" class="filter">
    </figure>
    <h1 class="card--title">{{item['title']}} </h1>

    <div class="container--flex">
        <div class="items--left">
            <p>Surface : {{item['living_area'] }} m²</p>
            <p v-if="item['type']==flat">Appartement à {{item['address'] }} ( {{item['address']['postal_code']}} )</p>
            <p v-else>Maison à {{item['address']['city']}} ( {{item['address']['postal_code']}} )</p>
        </div>
        <div class="items--right">
            <p class="price">  {{ item['full_rent_price'] }} €</p>
        </div>
        
    </div>
</template>

<style lang="scss" scoped>

    figure{
        position: relative;
        height: 300px;
        img{
            object-fit: cover;
            
        }
        .filter{
            position: absolute;
            top: 0px;
            left: 0px;
        }
    }
        
    .card--title{
        position: absolute;
        top: 20px;
        width: 250px;
        left: calc(50% - 125px);
        text-align: center;
        font-size: 1.25rem;
    }

    .container--flex{
        padding:10px;
        
        .items--right{
            margin-left: 20px;
        }
    }
</style>