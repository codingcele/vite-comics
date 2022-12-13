<script>
export default {
    name: "AppHeader",
}
</script>

<template>
    <header>
        <a href="/" class="brand">
            <img src="/dc-logo.png" alt="DC">
        </a>
    </header>
</template>

<style lang="scss" scoped>
/* scoped serve a dire che il css si riferirà solo all'header */
header {
    display: flex;
    justify-content: space-between;
}
</style>