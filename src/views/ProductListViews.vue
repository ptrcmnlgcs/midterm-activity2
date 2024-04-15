<template>
    <div>
        <!-- Use the ProductList component here -->
        <ProductList />
    </div>
</template>

<script>
// Import the ProductList component
import ProductList from '@/components/ProductList.vue';

export default {
    name: 'ProductListView',
    components: {
        ProductList
    }
}
</script>
