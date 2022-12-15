<script>
export default {
    name: "AppMerchandise",
    data() {
        return {
            links: [
                {
                    text: "DIGITAL COMICS",
                    source: "../assets/images/buy-comics-digital-comics.png",
                },
                {
                    text: "DC MERCHANDISE",
                    source: "#",
                },
                {
                    text: "SUBSCRIPTION",
                    source: "#",
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    source: "#",
                },
                {
                    text: "DC POWER VISA",
                    source: "#",
                },
            ],
        }
    }
}
</script>

<template>
    <div class="merchandise">
        <ul>
            <li v-for="(link, index) in links" :key="index">
                <img :src="link.source" alt="">
                <a :href="link.source">{{ link.text }}</a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
div {
    display: flex;
    height: 16vh;
    background-color: rgb(2, 130, 249);
    padding: 0px 200px 0px 200px;

    ul {
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
        width: 100%;
        list-style-type: none;
        padding: 0px;

        li {
            display: flex;
            align-items: center;
            padding: 5px 10px;

            a {
                text-decoration: none;
                font-size: 10px;
                color: white;
            }
        }
    }
}
</style>