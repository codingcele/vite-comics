<script>
export default {
    name: "AppMerchandise",
    data() {
        return {
            links: [
                {
                    text: "DIGITAL COMICS",
                    source: "/buy-comics-digital-comics.png",
                },
                {
                    text: "DC MERCHANDISE",
                    source: "/buy-comics-merchandise.png",
                },
                {
                    text: "SUBSCRIPTION",
                    source: "/buy-comics-subscriptions.png",
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    source: "/buy-comics-shop-locator.png",
                },
            ],
        }
    }
}
</script>

<template>
    <div class="merchandise">
        <a href="/" v-for="(link, index) in links" :key="index">
            <img :src="link.source" alt="" class="scale">
            <span href="#">{{ link.text }}</span>
        </a>
        <a href="/">
            <img class="differentScale" src="../assets/buy-dc-power-visa.svg" alt="">
            <span href="#">DC POWER VISA</span>
        </a>
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

    a {
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
}

span {
    margin-left: 10px;
}
</style>