<script>
export default {
    name: "AppLoad",
}
</script>

<template>
    <div>
        <a href="/">
            LOAD MORE
        </a>
    </div>
</template>

<style lang="scss" scoped>
/* scoped serve a dire che il css si riferirà solo all'header */
div {
    display: flex;
    justify-content: center;
    padding: 15px;
    background-color: rgb(28, 28, 28);

    a {
        text-decoration: none;
        color: white;
        font-size: 10px;
        padding: 7px;
        width: 140px;
        background-color: rgb(2, 130, 249);
        text-align: center;
        font-weight: bold;
    }
}
</style>