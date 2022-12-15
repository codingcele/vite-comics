<script>
export default {
    name: "AppFooter",
    data() {
        return {
            links: [
                {
                    source: "../assets/images/footer-facebook.png",
                },
                {
                    source: "../assets/images/footer-twitter.png",
                },
                {
                    source: "../assets/images/footer-youtube.png",
                },
                {
                    source: "../assets/images/footer-pinterest.png",
                },
                {
                    source: "../assets/images/footer-periscope.png",
                },
            ],
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="leftFooter">
            SIGN-UP NOW!
        </div>
        <div class="rightFooter">
            <div class="follow">
                FOLLOW US
            </div>
            <img v-for="(link, index) in links" :key="index" :src=link.source alt="">
        </div>
    </div>
</template>

<style lang="scss" scoped>
/* scoped serve a dire che il css si riferirà solo all'header */
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 12vh;
    background-color: rgb(48, 48, 48);
    padding: 0px 200px 0px 200px;
    font-size: 13px;

    .leftFooter {
        color: white;
        border: 2px solid rgb(0, 134, 255);
        padding: 8px;
    }

    .rightFooter {
        display: flex;
        align-items: center;

        div {
            font-weight: bold;
            color: rgb(0, 134, 255);
        }
    }
}
</style>