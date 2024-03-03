<script>
    import axios from 'axios';
    import SingleCocktail from '../components/SingleCocktail.vue';
    import CocktailsAside from '@/components/CocktailsAside.vue';

    export default {
    name: "CocktailsView",
    components: {
    SingleCocktail,
    CocktailsAside
},

    data() {
        return {
            cocktails: [],
            category: -1,
        }
    },

    methods: {
        getCocktails(newCategory){
            axios.get('http://127.0.0.1:8000/api/cocktails', {
                params: {
                    category: newCategory,
                }
            })
            .then((response) => {
                console.log(response.data.results);
                this.cocktails = response.data.results;
            })
            .catch(function (error) {
                console.log(error);
            });  
        },
        CategoryFilterHandler(category) {
            console.log('CIAONE');
            this.getCocktails(category);
        }
    },

    created() {
        this.getCocktails(this.category);
    },
    }
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-12">
                <h1 class="text-center py-3">Cocktails</h1>
            </div>
            <div class="col-12 mb-3">
                <button class="btn btn-primary" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvas" aria-controls="offcanvas">Filters</button>
            </div>
            <div class="col-4" v-for="cocktail in cocktails">
                <SingleCocktail :cocktail = 'cocktail'/>
            </div>
        </div>
    </div>
    <CocktailsAside @CategoryFilter="CategoryFilterHandler"/>
</template>

<style lang="scss" scoped>

</style>