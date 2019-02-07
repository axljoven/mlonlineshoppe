<template>
    <div id="new-arrivals" class="section-lg">
        <div class="container-fluid">
            <div class="row">

                <!-- Swiper -->
                <div class="col-12 col-md-7">
                    <div class="swiper-container">
                        <div class="swiper-wrapper">   

                            <div class="swiper-slide" v-for="(product, index) in products" :key="index">
                                <Product :productOBJ="product" />
                            </div> <!-- swiper-slide -->

                        </div> <!-- swiper-wrapper -->
                    </div> <!-- swiper-container -->
                </div>

                <!-- Content -->
                <div class="col-12 col-md-5">
                    <Content :contentOBJ="content" />
                </div>


            </div> <!-- row -->
        </div> <!-- container-fluid -->
    </div> <!-- #new-arrivals -->
</template>

<script>
// Imports
import Content from '@/components/partials/Content'
import Product from '@/components/partials/Product'
import productsJSON from '@/database/products.json'

export default {
    name: 'NewArrivals',
    components: {
        Product,
        Content,
    },
    data() {
        return {
            products: [],
            content: {
                additionalClass : '',
                preheader: 'New Arrivals',
                header: 'New products have arrived',
                desc: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam'
            }
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

    mounted() {
        let newArrivalsSwiper = new Swiper('#new-arrivals .swiper-container', {
            slidesPerView: 2,
            spaceBetween: 30,
            loop: true,
            autoplay: {
                delay: 4000
            },
        });
    }
}
</script>

<style></style>
