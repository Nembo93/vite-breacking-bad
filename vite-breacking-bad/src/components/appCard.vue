<script>
export default {
    name : "appCard",
    props: {
        info: Object,
    },
};
</script>

<template>
    <div class="card">
        <img src="">
        <h4>{{info.name}}</h4>
        <h5>Breacking Bad</h5>
        <h6>Alive</h6>
    </div>
</template>

<style>
.card{
    width: calc((100% / 5) - 20px);
    height: 200px;
    background-color: red;
    margin-bottom: 10px;
}
</style>