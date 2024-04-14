<template>
    <div>
      <ProductList :biscuits="biscuitProducts" />
    </div>
  </template>
  
  <script>
  import ProductList from './ProductList.vue';
  
  export default {
    name: 'BiscuitPage',
    components: {
      ProductList
    },
    data() {
      return {
        biscuitProducts: [
          {
            id: 1,
            name: 'Chocolate Chip Cookies',
            description: 'Classic chocolate chip cookies with chunks of chocolate.',
            price: 5.99
          },
          {
            id: 2,
            name: 'Shortbread Biscuits',
            description: 'Buttery and crumbly shortbread biscuits.',
            price: 3.49
          },
          {
          id: 3,
          name: 'Oatmeal Raisin Cookies',
          description: 'Chewy oatmeal cookies with sweet raisins.',
          price: 4.99
        },
        {
          id: 4,
          name: 'Digestive Biscuits',
          description: 'Whole wheat biscuits with a hint of sweetness, perfect for tea time.',
          price: 2.49
        },
        {
          id: 5,
          name: 'Gingerbread Cookies',
          description: 'Spiced cookies with ginger, cinnamon, and cloves, great for the holidays.',
          price: 3.99
        },
        {
          id: 6,
          name: 'Coconut Macaroons',
          description: 'Chewy coconut cookies with a crispy exterior, gluten-free and delicious.',
          price: 6.49
        }

      ]
     };
    }
  };
</script>
  


  
<style scoped>
.biscuit-page {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.page-title {
  font-size: 28px;
  color: #333;
  margin-bottom: 20px;
  text-align: center;
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}

.product {
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
  background-color: #f9f9f9;
}

.product h2 {
  font-size: 18px;
  color: #333;
  margin-bottom: 10px;
}

.product p {
  font-size: 14px;
  color: #666;
}

.product .price {
  font-size: 16px;
  color: #007bff;
  margin-top: 10px;
}
</style>