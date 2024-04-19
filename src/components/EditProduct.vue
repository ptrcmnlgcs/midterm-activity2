<template>
    <div>
      <h2>Edit Product</h2>
      <form @submit.prevent="updateProduct">
        <label>Name:</label>
        <input type="text" v-model="editedProduct.name" required><br>
        
        <label>Description:</label>
        <textarea v-model="editedProduct.description" required></textarea><br>
        
        <label>Price:</label>
        <input type="number" v-model="editedProduct.price" required><br>
        
        <button type="submit">Update</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    props: ['product'],
    data() {
      return {
        editedProduct: { ...this.product }
      };
    },
    methods: {
      updateProduct() {
        // Update product in the database or emit an event to parent component
        // For simplicity, let's emit an event
        this.$emit('update', this.editedProduct);
      }
    }
  };
  </script>
  