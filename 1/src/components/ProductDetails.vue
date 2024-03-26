<template>
    <div class="container">
        <div v-for="product in products" :key="product.name" class="product">
            <img :src="product.img" alt="">
            <h1>Наименование товара: </h1>
            <p>{{ product.name }}</p>
            <h2 v-if="product.available">Available</h2>
            <h2 v-else>Out of Stock</h2>
            <h2>Цена: {{ formattedPrice(product) }}</h2>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductDetails',

    data() {
        return {
            products: [
                { img: require('../assets/phone.png'), name: 'phone', price: 100, available: false },
                { img: require('../assets/mouse.jpg'), name: 'mouse', price: 50, available: true },
            ]
        }
    },

    computed: {
        formattedPrice() {
            return function (product) {
                return '$' + product.price.toFixed(2);
            };
        }
    },

    mounted() {

    },
}
</script>
<style scoped>
.container {
    display: flex;
    flex-direction: column;
}

.product {
    border: 1px solid #010000;
    padding: 10px;
    margin-bottom: 10px;
}

img {
    width: 30%;
    margin: 40px;
    padding: 15px;
}
</style>