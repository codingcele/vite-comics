<script>
export default {
    name: "AppMerchandise",
    data() {
        return {
            links: [
                {
                    text: "DIGITAL COMICS",
                    source: "../assets/images/buy-comics-digital-comics.png",
                    current: false,
                },
                {
                    text: "DC MERCHANDISE",
                    source: "#",
                    current: true,
                },
                {
                    text: "SUBSCRIPTION",
                    source: "#",
                    current: false,
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    source: "#",
                    current: false,
                },
                {
                    text: "DC POWER VISA",
                    source: "#",
                    current: false,
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
                <img :src=link.source alt="">
                <a :href="link.source">{{ link.text }}</a>
            </li>
        </ul>
    </div>
</template>

<style scoped>
.merchandise {
    height: 100px;
    background-color: rgb(2, 130, 249);
    padding: 0px 200px 0px 200px;
}



ul {
    display: flex;
    flex-direction: row;
    list-style-type: none;
    padding: 0px;
}

li {
    display: flex;
    align-items: center;
    padding: 5px 10px;
}

a {
    text-decoration: none;
    font-size: 10px;
    color: black;
}
</style>