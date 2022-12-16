<script>
export default {
    name: "AppHeader",
    data() {
        return {
            source: "/dc-logo.png",
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: false,
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
    },
    methods: {
        clicked(index) {
            let i = 0;
            while (i < this.links.length) {
                if (index != i) {
                    this.links[i].current = false;
                }
                i++;
            }
            this.links[index].current = true;
            console.log(this.links[index].current);
        },
    }
}

</script>

<template>
    <header>
        <a href="/" class="brand">
            <img :src="this.source" alt="DC">
        </a>

        <div>
            <ul id="changeColor">
                <li v-for="(link, index) in links" :key="index" @click="clicked(index)"
                    :class="{ lowborder: this.links[index].current }">
                    <a :class="{ click: this.links[index].current }" :href="link.url">{{ link.text }}</a>
                </li>
            </ul>

        </div>
    </header>
</template>

<style lang="scss" scoped>
/* scoped serve a dire che il css si riferirà solo all'header */

header {
    display: flex;
    justify-content: space-between;
    height: 12vh;
    padding: 0px 200px 0px 200px;

    a {
        display: flex;
        align-items: center;
        text-decoration: none;
        font-size: 10px;
        color: black;

        img {
            height: 60px;
        }
    }

    div {
        display: flex;

        ul {
            display: flex;
            flex-direction: row;
            list-style-type: none;
            padding: 0px;

            li {
                display: flex;
                align-items: center;
                padding: 5px 10px;
                cursor: pointer;
                margin-left: 5px;
            }
        }
    }
}

.click {
    color: rgb(2, 130, 249);
}

.lowborder {
    border-bottom: 4px solid rgb(2, 130, 249);
}
</style>