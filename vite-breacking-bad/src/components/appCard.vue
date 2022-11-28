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
    padding: 20px;
    background-color: rgb(46, 58, 70);
    margin-bottom: 10px;
    text-align: center;
}
.card_img{
    width: 100px;
    height: 150px;
}
.card h4{
    color: white;
}
.card h5, h6{
    color: gray;
}
.card h4{
    margin-top: 10px;
    margin-bottom: 20px;
}
</style>