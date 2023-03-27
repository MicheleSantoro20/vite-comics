<script>

    export default {
        name: "SignUpAndSocial",
        data () {
            return {
                Social: [
                {
                    type: "fa-brands",
                    socialtype: "fa-facebook",
                },
                {
                    type: "fa-brands",
                    socialtype: "fa-twitter",
                },
                {
                    type: "fa-brands",
                    socialtype: "fa-youtube",
                },
                {
                    type: "fa-brands",
                    socialtype: "fa-pinterest",
                },
                {
                    type: "fa-solid",
                    socialtype: "fa-location-dot",
                },
                ]
            }
        }
    }

</script>

<template>
    <div class="bg">
        <div class="wrapper">
            <button class="button">SIGN-UP NOW!</button>
            <div class="right">
                <div class="follow">FOLLOW US</div>
                <ul class="container-social">
                    <li v-for="element in Social" >
                        <i :class="[element.type, element.socialtype]">
                    </i>   
                </li>
            </ul>
            </div>

        </div>
    </div>


</template>

<style scoped lang="scss">
    @use "../styles/partials/mixin.scss";

    .bg {
        background-color: #303030;
        height: 150px;
    }
    .wrapper {
        @include mixin.page-margin;
        display: flex;
        justify-content: space-between;
        padding: 50px 0px;
    }

    .container-social {
        font-size: 40px;
        list-style: none;
        display: flex;
        gap: 30px;
    }

    i {
        object-fit: cover;
        border-radius: 50%;
        background-color: gray;
        padding: 5px;
        color: #303030;

        &:hover {
            background-color: white;
            cursor: crosshair;
        }
    }

    .right {
        display: flex;
        align-items: center;
        gap: 30px;
    }

    .follow {
        color: #0282f9;
        font-size: 25px;
        font-weight: bold;
    }
    
    .button {
        padding: 10px;
        border: 2px solid #0282f9;
        font-size: 20px;
        color: white;
        background-color: #303030;

        &:hover {
            background-color: gray;
            cursor: crosshair;
        }
    }
</style>