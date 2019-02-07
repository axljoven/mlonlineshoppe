<template>
    <div :class="['content', additionalClass]">
        <header>
            <div class="content-preheader">{{ preheader }}</div>
            <h2 class="content-header">{{ header }}</h2>
        </header>
        <p class="content-desc">{{ desc }}</p>
    </div>
</template>

<script>
export default {
    name: 'Content',
    data() {
        return {
            additionalClass: '',
            preheader : '',
            header : '',
            desc: ''
        }
    },
    created() {
        this.additionalClass = this.contentOBJ.additionalClass
        this.preheader = this.contentOBJ.preheader
        this.header = this.contentOBJ.header
        this.desc = this.contentOBJ.desc
    },
    props: {
        contentOBJ: Object
    }
}
</script>

