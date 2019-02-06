<template>
    <a :href="url" :class="['brand', navClass]" :alt="name">
        {{ name }}
    </a>
</template>

<script>
export default {
    name: 'Brand',
    mounted() {
                        
        //  Default for empty url
        if (this.url == null || this.url === '') {
            this.url = '/'
        }
    },

    props: {
        name: String,
        navClass: String,
        url: String,
    }
}
</script>

