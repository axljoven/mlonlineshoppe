<template>
    <div id="" class="slideshow">
        <div class="swiper-container">
            <div class="swiper-wrapper">
                <div v-for="(slide, index) in slides" :key="index" class="swiper-slide">
                    
                    <!-- Slide background image -->
                    <div class="slide-image" 
                        :style="{backgroundImage : 'url(' + require('@/assets/images/slideshow/' + slide.image)}">
                    </div>

                    <!-- SLide content -->
                    <Content :contentOBJ="{
                        additionalClass: '', 
                        preheader: slide.preheader, 
                        header: slide.header, 
                        desc: slide.content
                        }" 
                    />

                </div> <!-- swiper-slide -->
            </div> <!-- swiper-wrapper -->
        </div> <!-- swiper-container -->
    </div> <!-- #slideshow -->
</template>

<script>
import Content from '@/components/partials/Content'

export default {
    name: "Slideshow",
    components: {
        Content
    },
    data() {
        return {
            additionalClass: '',
            slides: []
        }
    },
    props: {
        slideshowOBJ: Object,
        params: Object
    },
    created() {
        this.additionalClass = this.slideshowOBJ.additionalClass
        this.slides = this.slideshowOBJ.items
    },
    mounted() {
        let slideshow = new Swiper('.slideshow > .swiper-container', {
            loop: true,
            effect: 'fade',
            autoplay : {
                delay: 5000
            }
        })

        console.log
    },
}
</script>
