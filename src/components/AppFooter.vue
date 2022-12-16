<script>
export default {
    name: "AppFooter",
    data() {
        return {
            links: [
                {
                    source: "/footer-facebook.png",
                },
                {
                    source: "/footer-twitter.png",
                },
                {
                    source: "/footer-youtube.png",
                },
                {
                    source: "/footer-pinterest.png",
                },
                {
                    source: "/footer-periscope.png",
                },
            ],
        }
    }
}
</script>

<template>
    <div class="container">
        <a href="#" class="leftFooter">
            SIGN-UP NOW!
        </a>
        <div class="rightFooter">
            <div>
                <a href="#">FOLLOW US</a>
            </div>
            <a href="#" v-for="(link, index) in links" :key="index">
                <img :src="link.source" alt="">
            </a>
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
            margin: 15px;

            a {
                font-weight: bold;
                color: rgb(0, 134, 255);
            }
        }

        a {
            margin: 7px;
        }

        img {
            height: 25px;
        }
    }
}

a {
    text-decoration: none;
}
</style>