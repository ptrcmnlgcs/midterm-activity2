<template>
    <div class="container">
      <h1>BISCUITS</h1>
      <table class="product-table">
        <thead>
          <tr>
            <th>Name</th>
            <th>Description</th>
            <th>Price</th>
            <th>Action</th> <!-- Added action column -->
          </tr>
        </thead>
        <tbody>
          <tr v-for="(biscuit, index) in biscuits" :key="index">
            <td>{{ biscuit.name }}</td>
            <td>{{ biscuit.description }}</td>
            <td>${{ biscuit.price }}</td>
            <td>
              <!-- <button @click="addToCart(biscuit)">Add </button> Example action button -->
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ProductList',
    props: {
      biscuits: {
        type: Array,
        required: true
      }
    },
    methods: {
      addToCart(biscuit) {
        // Implement your addToCart logic here
        console.log('Added', biscuit.name, 'to cart');
      }
    }
  };
  </script>
  
  <style scoped>
  .container {
    display: flex;
    flex-direction: column;
    align-items: center; /* Center items horizontally */
    justify-content: center; /* Center items vertically */
  }
  
  h1 {
    color: #333;
    font-size: 24px;
    margin-bottom: 20px;
  }
  .product-table {
  width: 100%;
  margin: 0 auto; /* Center the table horizontally */
  border-collapse: collapse;
}

.biscuit-page {
  max-width: 800px;
  margin: 20px auto; /* Center the page horizontally and add equal spacing on top and bottom */
  padding: 20px;
}
  .product-table {
    width: 100%;
    border-collapse: collapse;
  }
  
  .product-table th,
  .product-table td {
    border: 1px solid #ddd;
    padding: 8px;
  }
  
  .product-table th {
    background-color: #f2f2f2;
    text-align: left;
  }

  </style>
  