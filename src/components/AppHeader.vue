<script>
export default {
    name: "AppHeader",
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
    <header>
        <a href="/" class="brand">
            <img src="../assets/images/dc-logo.png" alt="DC">
        </a>

        <div>
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <a :class="{ active: link.current }" :href="link.url">{{ link.text }}</a>
                </li>
            </ul>

        </div>
    </header>
</template>

<style lang="scss" scoped>
/* scoped serve a dire che il css si riferirà solo all'header */
* {
    font-family: verdana;
}

header {
    display: flex;
    justify-content: space-evenly;
    height: 100px;

    a {
        display: flex;
        align-items: center;

        img {
            height: 70px;
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

                a {
                    text-decoration: none;
                    font-size: 12px;
                    color: black;
                }
            }
        }
    }
}
</style>