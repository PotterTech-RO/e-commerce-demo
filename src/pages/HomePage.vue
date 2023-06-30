<template>
    <div class="home-container">
        <div class="image-container">
            <img class="home-image" src="../assets/cover.jpeg" alt="">
            <div class="content">
                <h1 class="title">Unleash Your Retail Therapy.</h1><br>
                <p class="description">
                    Discover a world of endless possibilities with our vibrant e-commerce platform. Shop the latest trends,
                    find exclusive deals, and indulge in a seamless shopping experience.
                </p><br><br>
                <v-btn color="#FDD187" rounded="xl" size="x-large">Learn more</v-btn>

            </div>
        </div><br><br><br>
        <p class="text-left categories-title">Shop Our Top Categories</p>
        <div class="categories-container">
            <div class="category background-image-1">
                <p class="category-title">
                    Furniture
                </p>
            </div>
            <div class="category background-image-2">
                <p class="category-title">
                    Headphones
                </p>
            </div>
            <div class="category background-image-3">
                <p class="category-title">
                    Furniture
                </p>
            </div>
            <div class="category background-image-4">
                <p class="category-title">
                    Furniture
                </p>
            </div>
            <div class="category background-image-5">
                <p class="category-title">
                    Furniture
                </p>
            </div>
            <div class="category background-image-6">
                <p class="category-title">
                    Furniture
                </p>
            </div>
        </div><br><br><br>
        <p class="text-left categories-title">Most Viewed Products</p>
        <div class="products-list">
            <template v-for="index in [0, 1, 2, 3]" :key="index">
                <ProductCard :index="index" />
            </template>
        </div>
        <br><br>

    </div>
</template>

<script>
import { ref } from 'vue'
import ProductCard from '../components/ProductCard.vue'

export default {
    setup() {
        const count = ref(0)

        // expose to template and other options API hooks
        return {
            count
        }
    },
    components: {
        ProductCard
    },
    mounted() {
        console.log(this.count) // 0
    }
}
</script>

<style scoped>
.home-container {
    background-color: azure;
    height: 40rem;
}

.home-container .home-image {
    width: 100%;
    height: 40rem;
    object-fit: cover;
    display: flex;
    position: absolute;
}

.content {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: start;
    width: 40rem;
    margin: auto 7rem;
    text-align: start;
}

.content .title {
    font-size: 3rem;
}

.content .description {
    font-size: 1.4rem;
    font-weight: 400;
}

.image-container {
    height: 100%;
    display: flex;
    align-items: center;
}

.v-btn--variant-elevated {
    box-shadow: none;
}

.categories-container {
    overflow-x: auto;
    white-space: nowrap;
    margin: 0rem 7rem;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

.categories-title {
    font-size: 2rem;
    font-weight: 900;
    margin-left: 7rem;
    margin-bottom: 2rem;
}

.category {
    padding: 1rem;
    display: inline-block;
    width: 12.5rem;
    height: 15.75rem;
    background-color: #ddd;
    margin-right: 10px;
    border-radius: 0.8rem;
    cursor: pointer;
}

.background-image-1 {
    background-image: url('https://uploads-ssl.webflow.com/63e857eaeaf853471d5335ff/63e8c4e570738029a725e686_Furniture-min.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}

.background-image-2 {
    background-image: url('https://uploads-ssl.webflow.com/63e857eaeaf853471d5335ff/63e8c4e52d6553668075697e_hand%20bag-min.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}

.background-image-3 {
    background-image: url('https://uploads-ssl.webflow.com/63e857eaeaf853471d5335ff/63e8c4e460afc22b7ea53520_books-min.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}

.background-image-4 {
    background-image: url('https://uploads-ssl.webflow.com/63e857eaeaf853471d5335ff/63e8c4e754ac2e32897cb53b_tech-min.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}

.background-image-5 {
    background-image: url('https://uploads-ssl.webflow.com/63e857eaeaf853471d5335ff/63e8c4e64b769118272f244f_sneakers-min.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}

.background-image-6 {
    background-image: url('https://uploads-ssl.webflow.com/63e857eaeaf853471d5335ff/63e8c4e71eb4ad6d07e7568f_travel-min.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}

.category-title {
    font-size: 1.5rem;
    font-weight: 600;
    color: white;
}

.category-image {
    object-fit: cover;
    position: relative;
    width: 100%;
    height: 100%;
}

.products-list {
    margin: 0rem 7rem;
    display: flex;
    flex-direction: row;
    gap: 2rem;
    overflow-x: auto;

}
</style>