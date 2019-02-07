<template>
    <div id="home">
        <Slideshow :slideshowOBJ="slideshowOBJ" />
        <NewArrivals />
        <TopSellers />
        <About />
    </div>
</template>

<script>
// Imports
import Slideshow from '@/components/partials/Slideshow'
import NewArrivals from '@/components/partials/home/NewArrivals'
import TopSellers from '@/components/partials/home/TopSellers'
import About from '@/components/partials/home/About'
import SlideshowJSON from '@/database/slideshow.json'

export default {
    name: 'Home',
    data() {
        return {
            slideshowOBJ: {
                class: 'banner-slideshow',
                items: SlideshowJSON.slideshow,
            }
        }
    },
    components: {
        Slideshow,
        NewArrivals,
        TopSellers,
        About,
    }
}
</script>