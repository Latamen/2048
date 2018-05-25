
<template>
    <div class="board">
         <p>Score : </p>
        <table class="boardTable" border="1"> 
            <caption>Jeu 2048 ! :)</caption>
            <tr v-for="n in this.numberOfLines"> 
                <th></th> 
                <th></th> 
                <th></th> 
                <th></th> 
            </tr> 
        </table>   
    </div>
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

// Renvoie un nombre aléatoire entre un minimum et un maximum (inclus)
function getRandomInt(min, max) {
  min = Math.ceil(min);
  max = Math.floor(max);
  return Math.floor(Math.random() * (max - min)) + min;
}

console.log('Position de la 1ere case --> ' + getRandomInt(1, 4) + ' - ' + getRandomInt(1, 4));
// expected output: 0, 1 or 2
</script>

<style scoped>
.boardTable{
    margin-left: 25%;
}

th {
    height: 50px;
    width: 50px;
}
</style>