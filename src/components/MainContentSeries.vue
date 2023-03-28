<script>

    export default {
        name: "MainContentSeries",
        props: {
            img : String,
            title : String,
            prezzo : String,
            tipology : String
        }
    }

</script>

<template>

    <div class="wrapper">
        <div class="img-wrapper">
            <img class="series" :src="img" :alt="title">
            <div class="price-hover">
                <div> {{ prezzo }}</div>
            </div>
        </div>
        <div>
            <div> {{ title }}</div>
            <div> Category : <span class="type">{{ tipology }}</span> </div>
        </div>

    </div>

</template>

<style scoped lang="scss">
    @use "../styles/partials/mixin.scss";
    .series {
        height: 250px;
        width: 200px;


    }
    .wrapper {
        width: 100%;
        text-align: center;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;




    }
    .type  {
        color: #0282f9;
    }

    .price-hover {
        background-color: rgba($color: #0282f9, $alpha: 0.5);
        position: absolute;
        top: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        opacity: 0;
        height: 250px;
        width: 100%;
        font-size: 30px;
        transition: opacity 0.5s;

    }
.img-wrapper {
    position: relative;
    width: 200px;

    &:hover .price-hover{
            opacity: 1;


    }
}

</style>