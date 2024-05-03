<script>
</script>

<template>
    <div class="bg-black jumbotron">
        <div>
            <img src="../assets/img/jumbotron.jpg" alt="">
        </div>
    </div>
    <div class="cards w-80">

    </div>
</template>

<style lang = "scss" scoped>
/* Importo le classi dal file generals.scss */
@import '../style/generals.scss';
.bg-black {
    background-color : black;
    width : 100%;
    color : white;
}

.jumbotron{
    height: 450px;
    img{
        max-height: 450px;
        width: 100%;
        object-fit: fill;
    }
}
</style>