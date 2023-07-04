<template>
    <div>
        <h2> {{ product.name }}</h2>
        <p>Цена: {{ formattedPrice }}</p>
        <p>{{ product.available ? 'Available' : 'Out of stock' }}</p>
    </div>
</template>

<script>
export default {
    name: 'ProductDetails',
   props: {
        product: {
            type: Object,
            required: true,
            default: () => ({
                name: '',
                price: 0,
                available: false
            })
        }
    },
    data() {
        return {

        };
    },

    computed: {
        formattedPrice() {
            return `$${this.product.price}`;
        }
    },

    methods: {

    },
};
</script>

<style lang="scss" scoped></style>