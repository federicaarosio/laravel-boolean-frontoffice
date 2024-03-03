<script>
    import axios from 'axios'

    export default {
    name: "CocktailsAside",
    data() {
        return {
            categories: [],
            selectedCategory: -1,
        }
    },

    methods: {
        getCategories(){
            axios.get('http://127.0.0.1:8000/api/categories', {
                params: {
                }
            })
            .then((response) => {
                console.log(response.data.results);
                this.categories = response.data.results;
            })
            .catch(function (error) {
                console.log(error);
            });  
        },
        addCategoryFilter() {
            this.$emit('CategoryFilter', this.selectedCategory);
        }
    },

    created() {
        this.getCategories();
    },
    }
</script>

<template>
    <div class="offcanvas offcanvas-start" tabindex="-1" id="offcanvas" aria-labelledby="offcanvasLabel">
        <div class="offcanvas-header">
            <h5 class="offcanvas-title" id="offcanvasLabel">Cocktails Filter</h5>
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
        </div>
        <div class="offcanvas-body">
            <div>
            
            </div>
            <div class="dropdown mt-3">
                <label for="categories" class="form-label ps-1">Select a Categories</label>
                <select class="form-select" id="categories" v-model="selectedCategory" @change="addCategoryFilter">
                    <option value="-1">Select All</option>
                    <option v-for="category in categories" :value="category.id">{{ category.title }}</option>
                </select>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>