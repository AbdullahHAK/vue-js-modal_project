<template>
    <div class="modal-overlay" @click.self="closeModal">
        
      <div class="modal" :class="{sale: theme === 'sale'}">
        <slot>deafult content</slot> 
        <div class="actions">
            <slot name="links"></slot>
        </div>
        
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "Modal",
    props: {
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
  .modal .actions{
    text-align: center;
    margin: 30px 0 10px 0;
    color: #333;
  }
  .modal .actions a{
    color: #333;
    padding: 8px;
    border: 1px solid #eee;
    border-radius: 4px;
    text-decoration: none;
    margin: 10px;
  }
  </style>
  