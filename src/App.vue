<template>
  <h1>{{ title }}</h1>
  <button @click="showModal=true">show modal</button>
  <button @click="showModal2=true">show modal2</button>

  <Modal v-if="showModal2" theme="blahblah" @close="toggleModal2">
      <template v-slot:links>
        <a href="#">get a job</a>
        <a href="#">get a wife</a>
        <a href="#">get both</a>
      </template> 
      <h1>work hard for the giveaway</h1>
      <p>throw your degree cuz its of no use</p>
    </Modal>
  <Modal v-if="showModal" theme="blahblah" @close="toggleModal">
      <template v-slot:links>
        <a href="#">sign up</a>
        <a href="#">get degree</a>
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
      showModal2: false
    }
  },
  methods:{
    toggleModal(){
      this.showModal = !this.showModal
    },
    toggleModal2(){
      this.showModal2=!this.showModal2
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
