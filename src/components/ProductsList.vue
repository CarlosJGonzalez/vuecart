<template>
    <div v-if="cartItems.length > 0">
        <ProductsListItem 
            v-for="product in cartItems"
            :key="product.id"
            :product="product" />
    </div>
    <p v-else>You haven't added products to your cart yet!</p>
</template>

<script>
import ProductsListItem from './ProductsListItem.vue';
export default {
    name: 'ProductsList',
    props: ['cartItems'],
    components: {
        ProductsListItem,
    }
}
</script>

<style scoped>

</style>