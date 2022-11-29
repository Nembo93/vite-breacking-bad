<script>
import axios from 'axios';
import {store} from "../store";

import appCardVue from './appCard.vue';
import appSearchVue from './appSearch.vue';

export default {
    name: "appMain",
    components: {
        appCardVue,
        appSearchVue,
    },

    data() {
        return {
            store,
        };
    },

    // data() {
    //     return {
    //         characters: [],
    //     }
    // },

    methods: {
        changed (){
            console.log("cambiato!");
        }
    },

    mounted() {
    axios
      .get('https://www.breakingbadapi.com/api/characters')
      .then((response) => {
        this.store.characters = response.data;
      })
    }
};
    
</script>

<template>
    <div class="container">
        <div class="main_top">
            <appSearchVue onchange="changed"/>
        </div>

        <div class="main_box">
            <div class="founded">
                Founded 62 characters
            </div>

            <div class="card_container">
                <appCardVue
                v-for="character in store.characters"
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