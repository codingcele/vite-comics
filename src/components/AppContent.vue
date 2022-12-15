<script>
export default {
    name: "AppContent",
    data() {
        return {
            scritta: "--> Content goes here <--"
        }
    }
}
</script>

<template>
    <div class="content">
        <h3> {{ scritta }} </h3>
    </div>
</template>

<style scoped>
.content {
    display: flex;
    align-items: center;
    height: 14vh;
    padding: 0px 200px 0px 200px;
    background-color: rgb(28, 28, 28);
}

h3 {
    color: white;
}
</style>