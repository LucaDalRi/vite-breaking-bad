<script>
import axios from 'axios';
export default {
    name: 'Navbar',

    data() {
        return {
            arrArcheTypes: [],
        }
    },
    methods: {

    },
    mounted() {
        axios
            .get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then((risposta) => {
                for (let i = 0; i < 30; i++) {

                    this.arrArcheTypes.push(risposta.data.slice(0, 30)[i]);
                }
            })
    },
}
</script>

<template>

    <div class="row">
        <div class="col justify-content-center d-flex my-5">
            <div class="dropdown col-10 ">
                <select class="form-select" aria-label="Default select example">
                    <option selected>Arche Types</option>
                    <option :value="index" v-for="(tipi, index) in arrArcheTypes">
                        {{ arrArcheTypes[index].archetype_name }}
                    </option>
                </select>
            </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>

</style>