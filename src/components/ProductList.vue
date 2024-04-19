<template>
  <div class="container">
    <h1>BISCUITS</h1>
    <table class="product-table">
      <thead>
        <tr>
          <th>Name</th>
          <th>Description</th>
          <th>Price</th>
          <th>Action</th> 
        </tr>
      </thead>
      <tbody>
        <tr v-for="product in products" :key="product.name">
          <td>{{ product.name }}</td>
          <td>{{ product.description }}</td>
          <td>{{ product.price }}</td>
          <td>
            <button @click="editProduct(product)">Edit</button>
            <button @click="confirmDelete(product)">Delete</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { name: "Product A", description: "Description A", price: 10 },
        { name: "Product B", description: "Description B", price: 8 },
        { name: "Product C", description: "Description C", price: 12 }
      ],
      deletingIndex: null
    };
  },
  methods: {
    // eslint-disable-next-line no-unused-vars
    editProduct(product) {
    },
    confirmDelete(product) {
      if (confirm("Are you sure you want to delete this product?")) {
        this.deleteProduct(product);
      }
    },
    deleteProduct(product) {
      const index = this.products.indexOf(product);
      this.deletingIndex = index;
      setTimeout(() => {
        this.products.splice(index, 1);
        this.deletingIndex = null;
      }, 500);
    }
  }
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center; 
  justify-content: center;
}

h1 {
  color: #333;
  font-size: 24px;
  margin-bottom: 20px;
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

.product-table button {
  padding: 8px 16px; 
  border: none; 
  border-radius: 4px; 
  cursor: pointer; 
  margin-right: 8px; 
}

.product-table button:last-child {
  margin-right: 0;
}

/* Animation */
.product-table tbody tr.deleting {
  transition: opacity 0.5s;
  opacity: 0;
}
</style>
