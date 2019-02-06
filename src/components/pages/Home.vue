<template>
    <div id="home">
        <slideshow :slideshow="slideshow" />
        <new-arrival></new-arrival>
        <top-sellers></top-sellers>
        <about></about>
    </div>
</template>

<script>
// Imports
import Slideshow from '@/partials/home/Slideshow.vue'
import NewArrivals from '@/partials/home/NewArrivals.vue'
import TopSellers from '@/partials/home/TopSellers.vue'
import About from '@/partials/home/About.vue'
import SlideshowJSON from '@/database/slideshow.json'

export default {
    name: 'Home',
    data() {
        return {
            slideshow: SlideshowJSON.slideshow
        }
    },
    components: {
        'slideshow' : Slideshow,
        'new-arrival' : NewArrivals,
        'top-sellers' : TopSellers,
        'about' : About,
    }
}
</script>