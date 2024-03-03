<script>
    export default {
    name: "SingleCocktail",
    props: [
        'cocktail'
    ]
    }
</script>

<template>
    <div class="card mb-3">
        <div class="row g-0">
            <div class="col-md-4">
                <img :src="cocktail.img_url" class="img-fluid rounded-start" alt="...">
            </div>
            <div class="col-md-8 d-flex">
                <div class="card-body d-flex flex-column align-items-start justify-content-center">
                    <h5 class="card-title">{{ cocktail.name }}</h5>
                    <p class="card-text">{{ cocktail.category.title }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>

