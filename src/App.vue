<template>
  <h1>{{ title }}</h1>
  <button @click="showModal=true">show modal</button>

  <Modal v-if="showModal" :header="header" :offer="offer" theme="sale" @close="showModal=false"/>
  
</template>

<script> 
import Modal from './components/Modal'
export default {
  name: 'App',
  components: {
    Modal
  },
  data(){
    return{
      title: "my first vue app :))))",
      showModal: false,
      header: "sign up for the giveaway",
      offer: "grab your degree cuz its of no use"
    }
  }
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1{
  color: aqua;
}

</style>
