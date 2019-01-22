<template>
    <div id="slideshow" class="uk-position-relative" uk-slideshow="animation: fade; max-height: 600">
        
        <ul class="uk-slideshow-items">
            <li v-for="(slideshow, index) in slideshows" :key="index">
                <div class="content">
                    <div class="uk-container uk-container-large">
                        <h2 class="uk-text-small uk-margin-remove-bottom">{{ slideshow.category }}</h2>
                        <p class="uk-text-large uk-margin-remove-top uk-text-uppercase">{{ slideshow.header }}</p>
                        <p class="uk-width-1-3 uk-margin-medium-bottom">{{ slideshow.para }}</p>
                        <!-- <a class="" href="">Shop Now</a> -->
                        <router-link class="uk-button uk-button-default uk-button-large" to="/shop">Shop now</router-link>
                    </div>
                    <img :src="slideshow.image" alt="" uk-cover>
                </div>
            </li>
        </ul> <!-- uk-slideshow-items -->
        
        <!-- Controls -->
        <!-- <a class="uk-position-center-left uk-position-small uk-hidden-hover" href="#" uk-slidenav-previous uk-slideshow-item="previous"></a> -->
        <a class="uk-position-center-right uk-position-small uk-hidden-hover" href="#" uk-slidenav-next uk-slideshow-item="next"></a>

    </div> <!-- #slideshow -->
</template>

<script>
export default {
    name: "Slideshow",
    data() {
        return {
            slideshows: [
                {
                    category: 'Clothes',
                    header: 'Dress up',
                    para: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                    image: require('./../../../assets/images/slideshow/apparel-attire-blur.jpg') 
                },
                { 
                    category: 'Bags',
                    header: 'Bags that compliments you',
                    para: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                    image: require('./../../../assets/images/slideshow/apparel-boutique-colors.jpg') 
                },
                { 
                    category: 'Shoes',
                    header: 'Shoes you\'ll love',
                    para: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                    image: require('./../../../assets/images/slideshow/break-car-couple.jpg') 
                },
            ]
        }
    }
}
</script>

<style scoped>
</style>
