<template>
    <div id="about" class="">
        <div class="banner">
            <h1>About Us</h1>
            <a href="#about-content" uk-scroll><span uk-icon="icon: chevron-down;"></span></a>
        </div>

        <div id="about-content" class="section-lg uk-container uk-container-large">
            <div uk-grid>


                <div class="uk-width-1-2@m content">
                    <h2>Who we are</h2>
                    <p>
                        Lorem ipsum dolor sit amet, 
                        consectetur adipiscing elit, 
                        sed do eiusmod tempor incididunt 
                        ut labore et dolore magna aliqua. 
                        Amet luctus venenatis lectus magna 
                        fringilla urna. Ultrices tincidunt 
                        arcu non sodales. Pulvinar pellentesque 
                        habitant morbi tristique. Eu lobortis 
                        elementum nibh tellus molestie nunc 
                        non blandit massa. Adipiscing commodo 
                        elit at imperdiet dui accumsan. Diam 
                        maecenas sed enim ut. Id leo in vitae 
                        turpis. Tellus orci ac auctor augue 
                        mauris augue neque gravida. Eu facilisis 
                        sed odio morbi quis commodo odio. 
                        Aliquam malesuada bibendum arcu vitae. 
                        Orci nulla pellentesque dignissim enim 
                        sit amet venenatis urna cursus. Bibendum 
                        est ultricies integer quis auctor elit sed. 
                        Dui id ornare arcu odio ut sem nulla. Et 
                        sollicitudin ac orci phasellus egestas 
                        tellus. Purus in mollis nunc sed id semper risus in.
                    </p>

                    <p>Quis auctor elit sed vulputate mi sit amet mauris. Enim lobortis scelerisque fermentum dui faucibus in ornare quam viverra. In ante metus dictum at tempor commodo ullamcorper a. Erat imperdiet sed euismod nisi porta lorem. Lorem ipsum dolor sit amet consectetur adipiscing elit pellentesque habitant. Netus et malesuada fames ac turpis. Eu non diam phasellus vestibulum lorem sed risus. Aliquam sem et tortor consequat. Tortor condimentum lacinia quis vel eros donec. Et malesuada fames ac turpis egestas sed tempus urna et.</p>

                    <hr class="uk-margin-large-top">

                    <h2>Contact Us</h2>
                    <p>
                        Lorem, ipsum dolor sit amet consectetur 
                        adipisicing elit. Excepturi omnis iusto 
                        minus commodi
                    </p>
                    <form class="uk-form-stacked">
                        <div class="uk-margin">
                            <label class="uk-form-label" for="form-stacked-name">Full name</label>
                            <div class="uk-form-controls">
                                <input class="uk-input" id="form-stacked-name" type="text" placeholder="Your name here">
                            </div>
                        </div>
                        <div class="uk-margin">
                            <label class="uk-form-label" for="form-stacked-email">Email</label>
                            <div class="uk-form-controls">
                                <input class="uk-input" id="form-stacked-email" type="email" placeholder="Your email here">
                            </div>
                        </div>
                        <div class="uk-margin">
                            <label class="uk-form-label" for="form-stacked-message">Message</label>
                            <div class="uk-form-controls">
                                <textarea class="uk-textarea" id="form-stacked-message" rows="5" placeholder=""></textarea>
                            </div>
                        </div>
                        <button type="submit" class="uk-button uk-button-default">Submit</button>
                    </form>
                </div> <!-- uk-width -->


            </div> <!-- uk-grid -->
        </div> <!-- #about-content -->
    </div>
</template>

<script>
export default {
    name: "About",
    data: function() {
        return {

        }
    }
}
</script>
<style></style>
