<script>
export default {
    name: "AppCard",
    props: {
        cards: Object,
    }
}
</script>

<template>
    <div class="jumbotron">
        <a href="/" class="current">
            CURRENT SERIES
        </a>
    </div>
    <div class="cardsContainer">
        <a href="/" v-for="(card, index) in cards" :key="index" class="card">
            <img :src="card.thumb" alt="">
            <div class="title">
                {{ card.series.toUpperCase() }}
            </div>
        </a>
    </div>
</template>

<style lang="scss" scoped>
/* scoped serve a dire che il css si riferirà solo all'header */
.jumbotron {
    height: 47vh;
    background-image: url("/jumbotron.jpg");
    background-size: cover;

    a {
        color: white;
        font-weight: bold;
        background-color: rgb(2, 130, 249);
        text-align: center;
        position: relative;
        padding: 10px 20px;
        left: 200px;
        top: calc(47vh - 10px);
    }
}

.cardsContainer {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    background-color: rgb(28, 28, 28);
    padding: 30px 200px 10px 200px;

    .card {
        margin: 5px;
        margin-top: 15px;

        img {
            width: 120px;
        }

        .title {
            margin-top: 5px;
            max-width: 120px;
            font-size: 11px;
            color: white;
        }
    }
}

a {
    text-decoration: none;
}
</style>