<template>
    <ul :class="['navigation', navClass]">
        <li class="nav-item" v-for="(item, index) in items" :key="index">
            <a :href="item.url">
                <span v-if="item.isIconVisible" :class="['nav-icon', 'icon', item.icon]"></span>
                <span v-if="item.isNameVisible" class="nav-name">{{ item.name }}</span>
            </a>
        </li>
    </ul>
</template>

<script>
export default {
    name: 'Navigation',
    data() {
        return {
            navClass: '',
            items: []
        }
    },
    props: { 'nav' : Object },
    mounted() {

        this.navClass = this.nav.navClass
        this.items = this.nav.items
    }
}
</script>

