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
    
    <p class="card--title">{{item['title']}} </p>
    <div class="container--flex">
        <div class="items--left">
            <p>Surface : {{item['living_area'] }} m²</p>
            <p v-if="item['type']==flat">Appartement à {{item['address'] }} </p>
            <p v-else>Maison à {{item['address']['city']}} ( {{item['address']['postal_code']}} )</p>
        </div>
        <div class="items--right">
            <p>  {{ item['full_rent_price'] }} €</p>
            
        </div>
        
    </div>
</template>

<style lang="scss" scoped>

    figure{
        position: relative;
        img{
            width: 100%;
        }
    }
    .filter{
        position: absolute;
        top: 0px;
        left: 0px;
        
    }
    .card--title{
        position: absolute;
        top: 20px;
        width: 250px;
        left: calc(50% - 125px);
        text-align: center;
    }
    
    .items--left{

    }
    .items--right{
        margin-left: 20px;
        p{
            width: max-content;
            background-color: #3a4cbd;
            border-radius: 50px;
            padding: 2px 10px;
        }
    }


</style>