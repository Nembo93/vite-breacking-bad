<script>
import appCardVue from './appCard.vue';
import axios from 'axios';
export default {
    name: "appMain",
    components: {
        appCardVue,
    },
    mounted() {
    axios
      .get('https://www.breakingbadapi.com/api/characters')
      .then((response) => {
        console.log(response)
      })
    }
};
</script>

<template>
    <div class="container">
        <div class="main_top">
            <select id="">
                <option value="">Select category</option>
            </select>
        </div>

        <div class="main_box">
            <div class="founded">
                Founded 62 characters
            </div>

            <div class="card_container">
                <appCardVue/>
            </div>

        </div>
    </div>
</template>

<style>
.container{
    width: 800px;
    background-color: yellow;
    margin: auto;
    padding: 20px;
}
.main_top{
    background-color: darkblue;
    padding: 20px;
}
.main_box{
    background-color: white;
    height: 400px;
    padding: 20px;
}
.founded{
    margin: auto;
    width: 90%;
    background-color: black;
    color: white;
    font-size: 16px;
    padding: 10px;
}
.card_container{
    background-color: blueviolet;
    height: 300px;
    margin-top: 20px;
    padding: 20px;
}
</style>