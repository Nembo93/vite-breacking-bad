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
        <img  class="card_img" :src=info.img>
        <h4>{{info.name}}</h4>
        <h5>{{info.category}}</h5>
        <h6>{{info.status}}</h6>
    </div>
</template>

<style>
.card{
    width: calc((100% / 5) - 20px);
    height: 200px;
    background-color: red;
    margin-bottom: 10px;
    text-align: center;
}
.card_img{
    width: 100px;
    height: 100px;
}
</style>