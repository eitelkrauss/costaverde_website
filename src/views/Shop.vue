<template>
    <div>
        <div id="catalogue-container">
        <v-card class="catalogue-item " v-for="product,i in products" :key="i" dark :img="product.img">
            <!--<v-img :src="product.img" height="70%"></v-img>-->
            <v-card-title class="card-title">{{product.name}}</v-card-title>
            <v-card-subtitle style="text-align: left;">${{product.price}}</v-card-subtitle>
            <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn text><i class="fas fa-cart-plus plus-cart-icon"></i></v-btn>
            </v-card-actions>
        </v-card>
        </div>
    </div>
</template>

<script>
export default {
    name: "Shop",
    data() {
        return {
            products: [
                {
                    name: "Mangostan",
                    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse3.mm.bing.net%2Fth%3Fid%3DOIP.4M2oYqRF8Fp49NG1LAzTuAHaE8%26pid%3DApi&f=1",
                    unidad: "kg",
                    price: 15
                },
                {
                    name: "Manzana",
                    img: "https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Ftierrafertil.com.mx%2Fwp-content%2Fuploads%2F2017%2F08%2FMANZANA-COAHUILA.jpg&f=1&nofb=1",
                    price: 0.45,
                    unidad: "u"
                },
                {
                    name: "Papaya Hawaiiana",
                    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse3.mm.bing.net%2Fth%3Fid%3DOIP.4qLku0eq4uQBnaotX3gI-AHaE8%26pid%3DApi&f=1",
                    price: 2,
                    unidad: "u"
                },
                {
                    name: "Mango",
                    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fagronomag.com%2Fwp-content%2Fuploads%2F2020%2F02%2Fglenn-mango.jpg&f=1&nofb=1",
                    price: 3,
                    unidad: "kg"
                }
            ]
        }
    }
}
</script>

<style scoped>
    #catalogue-container {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        padding: 2rem;
    }

    .catalogue-item {
        width: 100vw;
        max-width: 400px;
        height: 500px;
        margin-top: 1rem;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
    }

    .card-title {
        font-weight: 800;
        font-size: 2rem;
        text-shadow: 3px 3px black;
        word-break: keep-all;
        line-height: 2.5rem;
    }

    .plus-cart-icon {
        font-size: 1.8rem;
        margin: .5rem;
    }


@media(min-width: 900px){
    .catalogue-item {
        margin: 2rem;
    }
}


</style>

