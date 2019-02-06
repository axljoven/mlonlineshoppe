<template>
    <div id="top-sellers" class="section-lg">
        <div class="uk-container uk-container-large">
            <div class="uk-grid-medium" uk-grid>

                <!-- Header -->
                <div class="uk-width-1-2@s uk-width-1-4@m pr-80">
                    <h2 class="uk-text-small uk-margin-remove-bottom">Top Sellers</h2>
                    <p class="uk-text-large uk-margin-remove-top uk-text-uppercase">Lorem ipsum dolor</p>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
                        sed do eiusmod tempor incididunt ut labore et dolore magna 
                        aliqua. Ut enim ad minim veniam
                    </p>
                    <router-link class="uk-button uk-button-default uk-margin-small-top" to="/shop">Shop Now</router-link>
                </div>

                <!-- Products -->
                <div v-for="(product, key) in products" class="uk-width-1-2@s uk-width-1-4@m uk-text-center" :key="key">
                    <div class="uk-card uk-card-default uk-card-body py-40" :style="{ 'background-color' : product.color }">
                        <div class="uk-card-media-top">
                            <img uk-img width="60%" :src="require('./../../../assets/images/products/' + product.image)" alt="">
                        </div>
                        <div class="uk-card-body">
                            <h3 class="uk-card-title ">{{ product.name }}</h3>
                            <a href="" class="uk-link-text">Add to cart</a>
                        </div>
                    </div>
                </div>
                

            </div> <!-- uk-grid -->
        </div> <!-- uk-container -->
    </div> <!-- #top-sellers -->
</template>

<script>
// Products
import productsJSON from './../../../database/products.json'

export default {
    name: 'TopSellers',
    data() {
        return {
            products: []
        }
    },
    created: function() {
        // Get 2 products
        this.products = productsJSON.filter(function(prod) {
            if ( prod.id == 14 || prod.id == 9 || prod.id == 2 ) {
                return {
                    name: prod.name,
                    category: prod.category,
                    desc: prod.description,
                    price: prod.price,
                    image: prod.image
                }
            }
        });
    },
}
</script>

<style>

</style>
