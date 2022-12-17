<script>
export default {
    name: "AppLists",
    data() {
        return {
            categories: [
                {
                    title: "DC COMICS",
                    links: [
                        {
                            text: "Characters",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Comics",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Movies",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "TV",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Games",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Videos",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "News",
                            url: "#",
                            current: false,
                        },
                    ],
                },
                {
                    title: "SHOP",
                    links: [
                        {
                            text: "Shop DC",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Shop DC Collectibles",
                            url: "#",
                            current: false,
                        },
                    ],
                },
                {
                    title: "DC",
                    links: [
                        {
                            text: "Terms Of Use",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Privacy policy (New)",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Ad Choices",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Advertising",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Jobs",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Subscriptions",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Talent Workshops",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "CPSC Certificates",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Ratings",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Shop Help",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "Contact Us",
                            url: "#",
                            current: false,
                        },
                    ],
                },
                {
                    title: "SITES",
                    links: [
                        {
                            text: "DC",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "MAD Magazine",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "DC Kids",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "DC Universe",
                            url: "#",
                            current: false,
                        },
                        {
                            text: "DC Power Visa",
                            url: "#",
                            current: false,
                        },
                    ],
                },
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="left">
            <div v-for="(category, index) in categories" :key="index" class="list">
                <div class="titleContainer">
                    <a href="/" class="title">
                        {{ category.title }}
                    </a>
                </div>
                <div v-for="(link, index) in category.links" :key="index">
                    <a href="/" class="item">
                        {{ link.text }}
                    </a>
                </div>
            </div>
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

    .left {
        display: flex;
        flex-direction: column;
        height: 40vh;
        width: calc(100% - 45vh - 400px);
        flex-wrap: wrap;

        .list {
            margin-right: 30px;
            margin-bottom: 15px;

            .titleContainer {
                margin-top: 5px;
                margin-bottom: 5px;

                .title {
                    font-size: 14px;
                    font-weight: bold;
                    color: white;
                }
            }


            .item {
                font-size: 10px;
                color: gray;
                margin-bottom: 2px;
            }
        }

    }

    .right {
        height: 100%;
        width: 65vh;
        background-image: url("./public/dc-logo-bg.png");
        background-size: 65vh;
        background-position: center;
    }
}

a {
    text-decoration: none;
}
</style>