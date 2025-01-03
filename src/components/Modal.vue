<template>
    <div class="modal-overlay" @click.self="closeModal">
        <!-- now modal is only closing when i click outside not on it -->
      <div class="modal" :class="{sale: theme === 'sale'}">
        <h1>{{ header }}</h1>
        <p>{{ offer }}</p>
        <!-- to react on certain events we use click event modifiers -->
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "Modal",
    props: {
        header: String,
        offer: String,
        theme: String
    },
    methods: {
        closeModal(){
            this.$emit('close')
        }
    }
  }
  </script>
  
  
  <style>    
  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .modal {
    background: white;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
  }
  
  .modal h1{
    color: blue;
  }
  .modal.sale{
    background: red;
    color: white;
  }
  .modal.sale h1{
    color: white;
  }
  </style>
  