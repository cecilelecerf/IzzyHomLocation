<script>
    export default {
        name: 'Search',
    }
</script>

<template>
    <form action="" method="get"> 
        <section id="is_furnished">
            <h3>Meublé | Non Meublé</h3>
            <div class="container--flex row">
                <div>
                    <label for="furnished">Meublé</label>
                    <input type="radio" name="is_furnished" value="furnished" id="furnished">
                </div>
                <div>
                    <label for="not_furnished">Non meublé</label>
                    <input type="radio" name="is_furnished" value="not_furnished" id="not_furnished">
                </div>
            </div>
        </section>
    
        <section>
            <h3>Type de bien</h3>
            <div class="container--flex row">
                <div>
                    <label for="flat">Appartement</label>
                    <input type="radio" name="type" id="flat">
                </div>
                <div>
                    <label for="house">Maison</label>
                    <input type="radio" name="type" id="house">
                </div>
            </div>
        </section>

        <section>
            <label for="living_area">Surface habitanle (en m²)</label>
            <div>
                <input type="number" name="min_living_area" placeholder="Min">
                <input type="number" name="max_living_area" placeholder="Max" >
            </div>
        </section>    

        <section>
            <label for="full_rent_price">Loyer</label>
            <div>    
                <input type="number" name="min_full_rent_price" placeholder="Min" >
                <input type="number" name="max_full_rent_price" placeholder="Max" >
            </div>
        </section>

        <section>
            <button type="submit" name="Search">Rechercher</button>
            <button type="reset">Reset</button>
        </section>

   </form>
</template>


<style lang="scss" scoped>
section{
    width: 30%;
    margin: 20px calc(50% - 15%);

    &:last-child{
        display: flex;
        flex-direction: column;
        button{
            border-radius: 25px;
            padding: 10px 20px;
            width: 50%;
            margin: 20px calc(50% - 25%);
        }
        button:first-child{
            background-color: #3a4cbd;
            color: rgba(235, 235, 235, 0.64);
            font-weight: bold;
            width: 100%;
            margin: 0px;
            font-size: 1.25rem;
        }
    }

    h3, & > label{
        text-align: center;
        font-size: 1.2rem;
    }
    div div {
        margin-top: 20px;
        display: flex;
        flex-direction: column-reverse;
        

    }

}

</style>