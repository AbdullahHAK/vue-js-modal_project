<template>
    <div class="modal-overlay">
      <div class="modal">
        <h2>This is a modal</h2>
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
  </style>
  