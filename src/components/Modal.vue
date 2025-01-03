<template>
    <div class="modal-overlay">
      <div class="modal">
        <h1>This is a modal</h1>
        <p>Click outside or on the button to close it.</p>
        <button @click="$emit('close')">Close Modal</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "Modal"
  }
  </script>
  
  <!-- <style scoped> /* now values of modals h1 will not be affected by app's h1 values, vue adds a data tag with every element, however it might slow down ur performance */ -->
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
  /* this is another way which doesnt decrease ur performance cuz u r specific */
  .modal h1{
    color: blue;
  }
  </style>
  