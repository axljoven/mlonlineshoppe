<template>
    <div id="site-header" uk-sticky="sel-target: .uk-navbar-container; cls-active: uk-navbar-sticky">
    <nav class="uk-navbar-container" uk-navbar>

        <!-- Navbar left -->
        <div class="uk-navbar-left">
            <ul class="uk-navbar-nav">
                <li><router-link to="/">Home</router-link></li>
                <li><router-link to="/shop">Shop</router-link></li>
                <li><router-link to="/about">About</router-link></li>
            </ul>
        </div> <!-- navbar-left -->

        <div class="uk-navbar-center">
            <a href="/" class="uk-navbar-item uk-logo">M&amp;L Onlineshoppe</a>
        </div>

        <!-- Navbar right -->
        <div class="uk-navbar-right">
            <ul class="uk-navbar-nav">
                <li class="uk-active"><a href="#" uk-icon="icon: cart"></a></li>
            </ul>
        </div> <!-- navbar-right -->
    </nav>
    </div>
</template>

<script>
    
</script>

<style scoped>

</style>
