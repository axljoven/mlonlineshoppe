<template>
    <footer id="site-footer" class="section-sm">
        
            <!-- Brand -->
            <Brand :name="brand.name" :url="brand.url" :navClass="brand.class" />

            <!-- Navigation -->
            <Navigation :nav="footerNav" />

            <!-- Copyright -->
            <p class="copyright" v-html="copyright"></p>

    </footer>
</template>

<script>
// Import
import Brand from '@/components/partials/Brand'
import Navigation from '@/components/partials/Navigation'

export default {
    name: 'Footer',
    data() {
        return {
            brand: {
                name: 'M&L Onlineshoppe',
                navClass: '',
                url: '/'
            },
            footerNav: {
                navClass: 'footer-navigation',
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
            copyright: `&copy; Copyright 2019 | M&L Onlineshoppe`
        }
    },
    components: {
        Brand,
        Navigation
    }
}
</script>

