<template>
  <h1>{{ title }}</h1>
  <button @click="showModal=true">show modal</button>

  <Modal v-if="showModal" theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">sign up</a>
        <a href="#">get degree</a>
        <!-- name slots, u must mention their name in child component where u want to use it -->
      </template> 
      <h1>sign up for the giveaway</h1>
      <p>grab your degree cuz its of no use</p>
    </Modal>
  
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
  },
  methods:{
    toggleModal(){
      this.showModal = !this.showModal
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
