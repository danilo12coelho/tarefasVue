<template>
  <div id="app">
    <h1>Tarefas</h1>
    <TaskGrid :tasks="tasks"/>
  </div>
</template>

<script>
import TaskGrid from './components/TaskGrid.vue'

export default {
  components: {TaskGrid},
  name: 'app',
    data(){
      return{
        tasks:[
          {name: "comprar remedios", pending: false},
          {name: "passear com o carrocho", pending: true}
        ]
      }
    }
  }
</script>

<style>
body {
  background: #283048;  /* fallback for old browsers */
  background: -webkit-linear-gradient(left, #859398, #283048);
  background: -o-linear-gradient(left, #859398, #283048);
  background: linear-gradient(to right, #859398, #283048);  /* Chrome 10-25, Safari 5.1-6 */ /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

#app{
  display: flex;
  flex: 1;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
#app h1{
  margin-bottom: 5px;
  font-weight: 300;
  font-size: 5rem;
}
</style>
