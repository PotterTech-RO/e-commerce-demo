<template>
    <div class="product-card">
        <div class="image-section">
            <div class="favourite-button">
                <v-icon icon="mdi-heart-outline"></v-icon>
            </div>
        </div>
        <div class="product-title">
            <p class="title">Wireless Earbuds, IPX8</p>
            <p class="price">$89.00</p>
        </div>
        <div class="product-description">
            <p>Organic Cotton, fairtrade certified</p>
        </div>
        <div class="product-rating">
            <template v-for="index in [0, 1, 2, 3, 4]" :key="index">
                <v-icon :icon="index > 3 ? 'mdi-star-outline' : 'mdi-star'"></v-icon>
            </template>
        </div>
        <v-btn color="#FDD187" rounded="xl" max-width="10rem">Add to cart</v-btn><br>

    </div>
</template>

<script>
import { reactive, toRefs } from 'vue'

export default {
    setup() {
        const state = reactive({
            count: 0,
        })

        return {
            ...toRefs(state),
        }
    }
}
</script>

<style scoped>
.product-card {
    display: flex;
    flex-direction: column;
    border-radius: 0.8rem;
}

.image-section {
    flex-grow: 4;
    text-align: right;
    width: 20rem;
    height: 20rem;
    padding: 1rem;
    background-image: url('../assets/headphones3.jpeg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    border-radius: 0.8rem;
}

.details-section {
    background-color: bisque;
    flex-grow: 1;
    display: flex;
}

.favourite-button {
    padding: 0.6rem;
    cursor: pointer;
    border-radius: 10rem;
    background-color: white;
    float: right;
}

.product-title {
    font-size: 1.2rem;
    font-weight: 800;
    margin-top: 0.6rem;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

.product-description {
    display: flex;
    font-size: small;
    font-weight: 500;
}

.product-rating {
    display: flex;
    margin-top: 0.6rem;
    margin-bottom: 1rem;
}
</style>