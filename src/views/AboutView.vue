<script>
    export default {
    name: "AboutView"
    }
</script>

<template>
    <div class="container mt-3">
        <div class="row justify-content-center ">
            <div class="col-12 mb-3">
                <h1 class="text-center">
                    About Us
                </h1>
            </div>
            <div class="col-12">
                <div class="row">
                    <div class="col-6">
                        <p class="text-end fs-5 ">
                            Benvenuti nel mondo affascinante e delizioso dei cocktails! Il nostro sito è un'oasi virtuale per gli amanti dell'arte della mixology, dove l'eleganza dei sapori si unisce alla creatività dei drink. Esplora la nostra vasta raccolta di ricette, dalle classiche agli innovativi mix contemporanei, e lasciati ispirare dalle nostre guide dettagliate su ingredienti, tecniche di miscelazione e decorazioni. Che tu sia un barman esperto o un principiante curioso, troverai qui tutto ciò di cui hai bisogno per creare e apprezzare cocktail straordinari. Unisciti a noi nel sollevare il calice alla bellezza e al piacere di un buon drink, perché ogni sorso racconta una storia di gusto e di convivialità.
                        </p>
                    </div>
                    <div class="col-6 position-relative my_col mb-4">
                        <img src="https://romeing.b-cdn.net/wp-content/uploads/2019/09/best-cocktail-establishments-in-rome-and-bartenders-770x513.jpg" class="img-fluid">
                        <img src="https://avatars.githubusercontent.com/u/3359943?v=4" class="my_img">
                    </div>
                    <div class="col-6 position-relative my_col">
                        <img src="https://www.finedininglovers.it/sites/g/files/xknfdk1106/files/2023-10/Edoardo%20Buono.jpg" class="img-fluid">
                        <img src="https://avatars.githubusercontent.com/u/3359943?v=4" class="my_img">
                    </div>
                    <div class="col-6">
                        <p class="fs-5">
                            In questo spazio dedicato alla cultura dei cocktail, ci impegniamo non solo a condividere ricette e consigli, ma anche a esplorare l'origine e la storia di ogni bevanda. Ogni cocktail ha una storia da raccontare, un viaggio che attraversa continenti e epoche, e noi siamo qui per far rivivere quei racconti attraverso il gusto e l'esperienza. Dalla tradizione artigianale alla moderna mixology, esploriamo le radici culturali di ogni bevanda, portandoti in un viaggio sensoriale attraverso i gusti e gli aromi del mondo dei cocktail. Unisciti a noi nell'esplorare l'arte e la scienza dietro ogni miscela, perché dietro ogni sorso c'è un universo di sapori da scoprire.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .my_img {
        width: 50%;
        display: none;
        border-radius: 50%;
    }

    .my_col:hover .my_img {
        display: inline-block;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
</style>