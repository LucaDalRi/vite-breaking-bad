<script>
export default {
    name: 'Navbar',
}
</script>

<template>

    <div class="row">
        <div class="col justify-content-center d-flex my-5">
            <div class="dropdown col-10 ">
                <button class="btn btn-light dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                    Alien
                </button>
                <ul class="dropdown-menu">
                    <li><a class="dropdown-item" href="#">Mostro</a></li>
                    <li><a class="dropdown-item" href="#">Casper</a></li>
                    <li><a class="dropdown-item" href="#">Fantasma Formaggino</a></li>
                </ul>
            </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>

</style>