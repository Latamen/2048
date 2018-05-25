
<template>
    <table class="board" border="1"> 
        <caption>Jeu 2048 ! :)</caption>
        <tr v-for="n in this.numberOfLines"> 
            <th></th> 
            <th></th> 
            <th></th> 
            <th></th> 
        </tr> 
    </table>   
</template>

<script>
import Board from "@/utils/Board"

export default {
  name: 'board',
  components: {},
  computed: {},
  methods: {
  },
  data (){
      return {
          grid: [],
          numberOfLines : 4
      }
  
  }
}
</script>

<style>
board{
    margin-left: 25%;
}

th {
    height: 50px;
    width: 50px;
}
</style>