<template>
  <div>
    <h2>{{ name }}</h2>
    <p>{{ player.score }}</p>
    <button @click= increase >Increase Score</button>
    <button @click= Decrease >Decrease Score</button>
  </div>
</template>

<script>
import { reactive } from "vue";

export default {
  props: {
    name: String ,
  },
  setup() {
    const player = reactive({
      score: 1,
    });
    const increase = () =>{
      player.score +=1;

    }
    const Decrease =() =>{
      player.score -=1
    }
    return {
      increase,
      Decrease,
      player,
    };
  },
};
</script>
