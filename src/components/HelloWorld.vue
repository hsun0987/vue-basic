<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h1>{{ message }}</h1>
    <!--<h1>{{ name }}</h1> -->
    <h1 :style="color" v-if="show">{{ name }}</h1>
    <h2 :style="`color : ${colors[0]}`">안녕</h2> 
    <h2 :style="`color : ${colors[1]}`">안녕</h2> 
    <h2 :style="`color : ${colors[2]}`">안녕</h2> 
    <h1 v-for="nation in nations" :key="nation">{{ nation }}</h1>
    <h1 v-for="(nation,idx) in nations" :key="idx">{{ idx + " " + nation }}</h1>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return{
      message : "키트리",
      name : "123",
      show : true,
      color : 'color : red',
      colors : ['red', 'blue', 'green'],
      nations : ['영국', '미국', '한국']
    }
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
