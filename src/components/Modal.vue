<template>
    <div class="modal-overlay">
      <div class="modal">
        <h1>{{ header }}</h1>
        <p>{{ offer }}</p>
        <!-- so what if we want to use modal for many times. ok but its content is fixed
         and for this problem we use props, to make our componenet more dynamic and reusable.
         2. what if many components want to use same user data array
         we cant hardcode it in every component, so we hardcode it
         prop r a way to pass data from a parent component like app to children component like modal-->
        <button @click="$emit('close')">Close Modal</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "Modal",
    props: {
        header: String,
        offer: String
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
  </style>
  