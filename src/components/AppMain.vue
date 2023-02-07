<script>
import axios from 'axios';

export default {
    data() {
        return {
            arrDeck: [],
        }

    },
    methods: {


    },
    mounted() {
        axios
            .get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
            .then((risposta) => {
                for (let i = 0; i < 30; i++) {
                    // mi dava fastidio che ci fosse un array nell`array
                    this.arrDeck.push(risposta.data.data.slice(0, 30)[i]);
                }
            })
    },
    name: "Main",

}
</script>

<template>

    <div class="row">
        <div class="col-10 offset-1">
            <div class="col-11 mx-5 bg-black text-light p-2">
                <h3>
                    Sono state trovate {{ arrDeck.length }} carte!
                </h3>
            </div>
            <div class="row">
                <div class="col-11 mx-5 d-flex flex-wrap">
                    <div class="card col-2 mb-3 mx-1" v-for="(carte, index) in arrDeck">
                        <div class="imgCard">
                            <img :src="arrDeck[index].card_images[0].image_url_small">
                        </div>
                        <div class="titoloCard text-light">
                            {{ arrDeck[index].name }}
                        </div>
                        <div class="tipoCard">
                            {{ arrDeck[index].type }}
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