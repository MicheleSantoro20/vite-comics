<script>

    export default {
        name: "FooterSection",
        data() {
            return {
                FooterNav : [
                    {
                        Name: "DC COMICS",
                        NavElement: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                    },
                    {
                        Name: "SHOP",
                        NavElement: ["Shop DC", "Shop DC Collectibles"]
                    },
                    {
                        Name: "DC",
                        NavElement: ["Terms of Use", "Privacy Policy (New)", "Ad Choiches", "Advertising", "jobs", "Subscriptions", "Talent Workshops", "CPSC", "Ratings", "Shop Help", "Contact Is"]
                    },
                    {
                        Name: "SITES",
                        NavElement: ["DC", "MAD Magazine", "DC Kid", "DC Universe", "DC Power Visa"]
                    },

                ]
            }
        }
    }

</script>

<template>
    <footer>
        <div class="wrapper">
            <div class="FooterList">
                <ul  class="Nav" v-for="element in FooterNav"> 

                    <li class="ListName">
                        {{element.Name}}
                        <ul>
                            <li class="ListItem" v-for="contenuti in element.NavElement">{{ contenuti }}</li>
                        </ul>
                    </li>
                </ul>
            </div>
            <div class="img-wrapper">
                <img src="../assets/dc-logo-bg.png" class="dc-img" alt="">
            </div>
        </div>
    </footer>

</template>

<style scoped lang="scss">
    @use "../styles/partials/mixin.scss";

    .wrapper {
        @include mixin.page-margin;
        display: flex;
        height: 350px;
    }

    footer {
        height: 350px;
        background-image: url(../assets/footer-bg.jpg);
    }
    li {
        color: white;
        list-style: none;
    }
    .FooterList {
        display: flex;
        width: 35%;
        height: 350px;
        flex-wrap: wrap;
        flex-direction: column;
        padding-top: 20px;
    }

    .Nav {
        display: flex;
        flex-wrap: wrap;
        flex-direction: column;
    }

    .ListName {
        width: 100%;
        padding: 5px;
        font-size: 30px;
        font-weight: bold;
    }

    .ListItem {
        font-size: 15px;
        font-weight: normal;
        color: gray;

        &:hover {
            color: white;
            cursor: crosshair;
        }
    }

    .img-wrapper {
        margin-left: 300px;
        overflow-y: hidden;
    }

    .dc-img {
        transform: translatey(-20%);
    }
</style>