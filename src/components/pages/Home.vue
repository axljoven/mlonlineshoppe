<template>
    <div id="home">
        <slideshow></slideshow>
        <new-arrival></new-arrival>
        <top-sellers></top-sellers>
        <about></about>
    </div>
</template>

<script>
// Slideshow
import Slideshow from './../partials/home/Slideshow.vue'
import NewArrivals from './../partials/home/NewArrivals.vue'
import TopSellers from './../partials/home/TopSellers.vue'
import About from './../partials/home/About.vue'

export default {
    name: 'Home',
    data() {
        return {
            data: {}
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

<style scoped>

</style>
