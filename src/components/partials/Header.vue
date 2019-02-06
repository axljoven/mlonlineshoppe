<template>
    <div id="site-header">

            <!-- Brand -->
            <Brand :name="brand.name" :url="brand.url" :navClass="brand.class" />


            <div>
                <!-- Main Navigation -->
                <Navigation :nav="mainNav" />

                <!-- Shop navigation -->
                <Navigation :nav="shopNav" />
            </div>

    </div>
</template>

<script>
// Import
import Navigation from '@/components/partials/Navigation'
import Brand from '@/components/partials/Brand'

export default {
    name: 'Header',
    data() {
        return {
            mainNav :{
                navClass: 'main-navigation',
                items : [
                    { 
                        name: 'Home', 
                        url: '/',
                        icon: null,
                        isNameVisible: true, 
                        isIconVisible: false, 
                    },
                    { 
                        name: 'Shop', 
                        url: '/shop',
                        icon: null,
                        isNameVisible: true, 
                        isIconVisible: false, 
                    },
                    { 
                        name: 'About', 
                        url: '/about',
                        icon: null,
                        isNameVisible: true, 
                        isIconVisible: false, 
                    }
                ],
            },
            shopNav : {
                navClass: 'shop-navigation',
                items: [
                    { 
                        name: 'Cart', 
                        url: 'javascript:void(0)',
                        icon: 'ion-ios-cart',
                        isNameVisible: false, 
                        isIconVisible: true, 
                    }
                ]
            },
            brand: {
                name: 'M&L Onlineshoppe',
                url: '/',
                class: ''
            }
        }
    },

    components: {
        Navigation,
        Brand
    }
}
</script>
