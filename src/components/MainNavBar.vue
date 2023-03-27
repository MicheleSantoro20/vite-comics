<script>

    export default {
        name: "MainNavBar",
        data () {
            return {
                MainNav: [
                    {
                        name: "DIGITAL COMICS",
                        img: "../src/assets/buy-comics-digital-comics.png",
                    },
                    {
                        name: "DC MERCHANDISE",
                        img: "../src/assets/buy-comics-merchandise.png",
                    },
                    {
                        name: "SUBSCRIPTION",
                        img: "../src/assets/buy-comics-subscriptions.png",
                    },
                    {
                        name: "COMIC SHOP LOCATOR",
                        img: "../src/assets/buy-comics-shop-locator.png",
                    },
                    {
                        name: "DC POWER VISA",
                        img: "../src/assets/buy-dc-power-visa.png",
                    },
                ]
            }
        }
    }

</script>

<template>
    <div class="MainNavBar ">
        <div class="container">
            <ul class="wrapper">
                <li class="mainNav" v-for="element in MainNav"> <img :src="element.img" class="img" alt=""> <div>{{ element.name }}</div> </li>
            </ul>
        </div>

    </div>


</template>

<style scoped lang="scss">
    @use "../styles/partials/mixin.scss";

    .wrapper {
        display: flex;
        justify-content: space-around;
        @include mixin.page-margin;
    }
    .MainNavBar {

        width: 100%;
        height: 200px;
        background-color: #0282f9;
    }
    .mainNav {
        
        color: white;
        display: flex;

        align-items: center;
        line-height: 200px;

        &:hover {
            color: gray;
            cursor: crosshair;
        }
    }

    .img {
        height: 60px;
    }

    .container {

        width: 100vw;
        margin: auto;
    }
</style>