<script>
import { store } from '../store.js'

export default {
    data() {
        return {
            store,
        }
    },
    name: "Main",

};
</script>

<template>

    <div class="row">
        <div class="col-10 offset-1">
            <div class="col-11 mx-5 bg-black text-light p-2">
                <h3>
                    Sono state trovate {{ store.arrDeck.length }} carte!
                </h3>
            </div>
            <div class="row">
                <div class="col-11 mx-5 d-flex flex-wrap">
                    <div class="card col-2 mb-3 mx-1" v-for="(carte, index) in store.arrDeck">
                        <div class="imgCard">
                            <img :src="store.arrDeck[index].card_images[0].image_url_small">
                        </div>
                        <div class="titoloCard text-light">
                            {{ store.arrDeck[index].name }}
                        </div>
                        <div class="tipoCard">
                            {{ store.arrDeck[index].type }}
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>
.col-10 {
    background-color: white;
}

.card {
    background-color: #d48f38;
    text-align: center;
    width: calc(100% / 6 - 8px);

    .imgCard img {
        width: 100%;
    }
}
</style>