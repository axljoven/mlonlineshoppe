<template>
    <div id="shop">

        <!-- Banner -->
        <div class="banner uk-background-fixed">
            <h1>Shop</h1>
            <a href="#archive-products" uk-scroll><span uk-icon="icon: chevron-down;"></span></a>
        </div>

        <!-- Products -->
        <div id="archive-products" class="products section-lg">
            <div class="uk-container uk-container-large">
                <div class="uk-grid-medium" uk-grid>

                        <div class="uk-width-1-3@m uk-text-center" v-for="(product, index) in products" :key="index">
                            <div class="uk-card uk-card-default uk-card-body py-40">
                                <div class="uk-card-media-top">
                                    <img uk-img width="60%" class="" :src="require('./../../assets/images/products/' + product.image)" alt="">
                                </div>
                                <div class="uk-card-body">
                                    <h3 class="uk-card-title ">{{ product.name }}</h3>
                                    <p>{{ product.description }}</p>
                                    <a href="" class="uk-button uk-button-default">Add to cart</a>
                                </div>
                            </div>
                        </div>
            
                </div><!-- uk-grid -->
            </div> <!-- uk-container -->
        </div> <!-- products -->

    </div>
</template>

<script>

// Products
import productsJSON from './../../database/products.json'
console.log(productsJSON)

export default {
    name: 'Shop',
    data() {
        return {
            products: productsJSON
        }
    },
    created: function() {
        // productsJSON.forEach(function(prod) {
        //     console.log(prod);
        //     this.products.push(prod);
        // });
    }
}
</script>

<style scoped></style>
