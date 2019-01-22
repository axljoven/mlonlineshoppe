<template>
    <div id="new-arrivals" class="section-lg">
        <div class="uk-container uk-container-large">
            <div class="uk-grid-medium" uk-grid>

                <!-- Products -->
                <div v-for="(product, key) in products" class="uk-width-1-3@m uk-text-center" :key="key">
                    <div class="uk-card uk-card-default uk-card-body py-40" :style="{ 'background-color' : product.color }">
                        <div class="uk-card-media-top">
                            <img uk-img width="60%" class="" :src="require('./../../../assets/images/products/' + product.image)" alt="">
                        </div>
                        <div class="uk-card-body">
                            <h3 class="uk-card-title ">{{ product.name }}</h3>
                            <p>{{ product.desc }}</p>
                            <a href="" class="uk-link-text">Add to cart</a>
                        </div>
                    </div>
                </div>
                
                <!-- Header -->
                <div class="uk-width-expand pl-80">
                    <h2 class="uk-text-small uk-margin-remove-bottom">New Arrivals</h2>
                    <p class="uk-text-large uk-margin-remove-top uk-text-uppercase">Lorem ipsum dolor</p>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
                        sed do eiusmod tempor incididunt ut labore et dolore magna 
                        aliqua. Ut enim ad minim veniam
                    </p>
                    <router-link class="uk-button uk-button-default uk-margin-small-top" to="/shop">Shop Now</router-link>
                </div>

            </div> <!-- uk-grid -->
        </div> <!-- uk-container -->
    </div> <!-- #new-arrivals -->
</template>

<script>

// Products
import productsJSON from './../../../database/products.json'

export default {
    name: 'NewArrivals',
    data() {
        return {
            products: []
        }
    },
    
    created: function() {

        // Get 2 products
        this.products = productsJSON.filter(function(prod) {
            if ( prod.id == 11 || prod.id == 7 ) {
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

<style></style>
