<template>
<div>
  <ul>
    <li v-for="character in characters" :key="character">
      {{character.name}}
    </li>
  </ul>
</div>

</template>

<script>
import { public_key, secret_key } from "../marvelous";
import axios from 'axios'
export default {
  name: "Characters",

    data(){
      return{
        characters:[]
      }
    },

    mounted(){
      this.getCharacters()
    },
  props: {},
  setup() {
  

    function getCharacters() {
      axios.get(`http://gateway.marvel.com/v1/public/characters?apikey=${public_key}`)
      .then((result)=>{
        //console.log(result)
        result.data.data.results.forEach((item)=>{
          console.log(item)
          this.characters.push(item) // lo metemos en el array de characters[]
        })

      })
      .catch((error)=>{
        console.log(error)
      })
    }

    return {
      getCharacters,
    };

  },
};
</script>

<style>
</style>