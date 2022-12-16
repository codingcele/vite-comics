<script>
export default {
    name: "AppLists",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: true,
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false,
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false,
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false,
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false,
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false,
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false,
                },
            ],
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="left">

        </div>
        <div class="right">
        </div>
    </div>
</template>

<style lang="scss" scoped>
/* scoped serve a dire che il css si riferirà solo all'header */
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 43vh;
    background-image: url("./public/footer-bg.jpg");
    padding: 0px 200px 0px 200px;


    .right {
        height: 100%;
        width: 65vh;
        background-image: url("./public/dc-logo-bg.png");
        background-size: 65vh;
        background-position: center;
    }
}
</style>