<script>
export default {
    name: "appHeader",
};
</script>

<template>
    <header>
        <img class="header_logo" src="../assets/logo.png" alt="logo">
        <h1 class="header_title">Breacking Bad Api</h1>
    </header>
</template>

<style scoped>
.header_logo{
    width: 50px;
    height: 25px;
} 
.header_title{
    display: inline-block;
    color: white;
}
</style>