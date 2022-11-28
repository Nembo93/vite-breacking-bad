<script>
import appCardVue from './appCard.vue';
import axios from 'axios';
export default {
    name: "appMain",
    components: {
        appCardVue,
    },

    data() {
        return {
            characters: [],
        }
    },

    mounted() {
    axios
      .get('https://www.breakingbadapi.com/api/characters')
      .then((response) => {
        console.log(response.data)
        this.characters = response.data;
        console.log(this.characters[0].name);
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
                <appCardVue
                v-for="character in characters"
                :info = "character"
                />
            </div>

        </div>
    </div>
</template>

<style>
.container{
    width: 1000px;
    /* background-color: yellow; */
    margin: auto;
    padding: 20px;
}
.main_top{
    background-color: rgb(46, 58, 70);
    padding: 20px;
}
.main_box{
    background-color: white;
    padding: 20px;
}
.founded{
    margin: auto;
    width: 98%;
    background-color: rgb(33, 37, 41);
    color: white;
    font-size: 16px;
    padding: 10px;
}
.card_container{
    /* background-color: blueviolet; */
    margin-top: 20px;
    padding: 20px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}
</style>