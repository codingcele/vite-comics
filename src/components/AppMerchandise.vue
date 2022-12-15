<script>
export default {
    name: "AppMerchandise",
    data() {
        return {
            links: [
                {
                    text: "DIGITAL COMICS",
                    source: "./public/buy-comics-digital-comics.png",
                },
                {
                    text: "DC MERCHANDISE",
                    source: "./public/buy-comics-merchandise.png",
                },
                {
                    text: "SUBSCRIPTION",
                    source: "./public/buy-comics-subscriptions.png",
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    source: "./public/buy-comics-shop-locator.png",
                },
            ],
        }
    }
}
</script>

<template>
    <div class="merchandise">
        <div v-for="(link, index) in links" :key="index">
            <img :src="link.source" alt="" class="scale">
            <a href="#">{{ link.text }}</a>
        </div>
        <div>
            <img class="differentScale" src="/buy-dc-power-visa.svg" alt="">
            <a href="#">DC POWER VISA</a>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.merchandise {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    background-color: rgb(2, 130, 249);
    padding: 0px 200px 0px 200px;
    height: 16vh;

    div {
        display: flex;
        align-items: center;
    }

    .scale {
        height: 40px;
    }

    .differentScale {
        height: 25px;
    }
}

a {
    text-decoration: none;
    font-size: 10px;
    color: white;
    margin-left: 10px;
}
</style>