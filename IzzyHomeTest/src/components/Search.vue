<script>
    export default {
        name: 'Search',
    }
</script>

<template>
    <form action="" method="get"> 
        <div>
            <label for="is_furnished">Meublé</label>
            <input type="radio" name="is_furnished" value="furnished" >
            <input type="radio" name="is_furnised" value="not_furnished" >
        </div>
    
        <div>
            <label for="type">Maison | Appartement</label>
            <input type="radio" name="type" >
            <input type="radio" name="type" >
        </div>
        <div>
            <label for="living_area">Surface habitanle (en m²)</label>
            <input type="number" name="min_living_area" placeholder="Min" >
            <input type="number" name="max_living_area" placeholder="Max" >
        </div>        
        <div>
            <label for="full_rent_price">Loyer</label>
            
            <input type="number" name="min_full_rent_price" placeholder="Min" >
            <input type="number" name="max_full_rent_price" placeholder="Max" >
        </div>
        <div>
            <button type="submit" name="Search">Rechercher</button>
            <button type="reset">Reset</button>
        </div>

   </form>
</template>


<style lang="scss" scoped>

</style>