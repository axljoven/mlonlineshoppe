<template>
    <div id="about-preview" class="section">
        <div class="container-fluid">

            <div class="box">
                <Content :contentOBJ="content" />

                <!-- <router-link class="uk-button uk-button-default uk-button-large uk-margin-small-top" to="/about">Learn More</router-link> -->
                <a href="/about">Learn More</a>
            </div> <!-- box -->
        
        </div> <!-- uk-container -->
    </div> <!-- #about-preview -->
</template>

<script>
// Imports
import Content from '@/components/partials/Content'

export default {
    name: "QuickAbout",
    components: {
        Content
    },
    data() {
        return {
            content: {
                additionalClass: '',
                preheader : 'About Us',
                header : 'Lorem ipsum dolor sit amit',
                desc: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam'
            }
        }
    }
}
</script>