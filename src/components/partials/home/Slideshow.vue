<template>
    <div id="" class="slideshow">
        
        <!-- <a class="" href="">Shop Now</a> -->
        <!-- <ul class="uk-slideshow-items">
            <li v-for="(slideshow, index) in slideshows" :key="index">
                <div class="content">
                    <div class="uk-container uk-container-large">
                        <h2 class="uk-text-small uk-margin-remove-bottom">{{ slideshow.category }}</h2>
                        <p class="uk-text-large uk-margin-remove-top uk-text-uppercase">{{ slideshow.header }}</p>
                        <p class="uk-width-1-3 uk-margin-medium-bottom">{{ slideshow.para }}</p>
                        <router-link class="uk-button uk-button-default uk-button-large" to="/shop">Shop now</router-link>
                    </div>
                    <img :src="slideshow.image" alt="" uk-cover>
                </div>
            </li>
        </ul> -->
        

        <div class="swiper-container">
            <div class="swiper-wrapper">
                <div v-for="(slide, index) in slideshow" :key="index" class="swiper-slide">
                    
                    <!-- Slide background image -->
                    <div class="slide-image">
                        <img :src="slide.image" alt="" />
                    </div>

                    <!-- SLide content -->
                    <div class="slide-content">
                        <header>
                            <div class="pre-header">{{ slide.category }}}</div>
                            <h2>{{ slide.header }}</h2>
                        </header>
                        <p>{{ slide.content }}</p>
                    </div>

                </div> <!-- swiper-slide -->
            </div> <!-- swiper-wrapper -->
        </div> <!-- swiper-container -->


        <!-- Controls -->

    </div> <!-- #slideshow -->
</template>

<script>
export default {
    name: "Slideshow",
    data() {
        return {}
    },
    props: {
        slideshow: Array
    }
}
</script>
