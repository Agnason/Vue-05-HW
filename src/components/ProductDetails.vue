<template>
    <div>

        <h2> {{ product.name }}</h2>
        <p>Цена: {{ formattedPrice }}</p>
        <template>
            <div>
                <p v-if="product.available">Available</p>
                <p v-else>Out of stock</p>
            </div>
        </template>
    </div>
</template>

<script>
export default {
    name: 'ProductDetails',
    props: {
        product: {
            name: String,
            price: Number,
            available: Boolean
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