<template>
    <div id="top-sellers" class="section-lg">
        <div class="container-fluid">
            <div class="row">
                
                <!-- Content -->
                <div class="col-12 col-md-4">
                    <Content :contentOBJ="content" />
                </div>

                <!-- Swiper -->
                <div class="col-12 col-md-8">
                    <div class="swiper-container">
                        <div class="swiper-wrapper">
                            
                            <div class="swiper-slide" v-for="(product, index) in products" :key="index">
                                <Product :productOBJ="product" />
                            </div> <!-- swiper-slide -->

                        </div> <!-- swiper-wrapper -->
                    </div> <!-- swiper-container -->
                </div>


            </div> <!--row -->
        </div> <!-- container-fluid -->
    </div> <!-- #top-sellers -->
</template>

<script>
// Imports
import Content from '@/components/partials/Content'
import Product from '@/components/partials/Product'
import productsJSON from '@/database/products.json'

export default {
    name: 'TopSellers',
    components: {
        Product,
        Content,
    },
    data() {
        return {
            products: [],
            content: {
                additionalClass : '',
                preheader: 'Top Sellers',
                header: 'Check our top-selling yet affordables goodies!',
                desc: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam'
            }
        }
    },
    created: function() {
        
        //
        // Get 3 products
        //

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
    mounted() {
        let topSellersSwiper = new Swiper('#top-sellers .swiper-container', {
            slidesPerView: 3,
            spaceBetween: 30,
            loop: true,
            autoplay: {
                delay: 4000
            },
        });
    }
}
</script>
