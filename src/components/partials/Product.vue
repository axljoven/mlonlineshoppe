<template>
    <div class="product">
        <img :src="require('@/assets/images/products/' + image)" alt="" class="product-thumbnail">
        <p class="product-name">{{ name }}</p>
        <p class="product-price">{{ price | currency }}</p>
        <a class="product-add-to-cart" href="javascript:void(0)">Add to cart</a>
    </div>
</template>

<script>
export default {
    name: 'Product',
    props: {
        productOBJ: Object
    },
    date() {
        return {
            name: '',
            image: '',
            price: ''
        }
    },
    created() {
        this.name = this.productOBJ.name
        this.image = this.productOBJ.image
        this.price = this.productOBJ.price
    },
    filters: {
        currency(value) {
            return 'Php ' + value
        }
    }
}
</script>

