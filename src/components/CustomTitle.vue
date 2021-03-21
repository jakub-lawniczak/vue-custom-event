<template>
    <div class="">
        <input type="text" v-model="value" @input="customTitle">
        {{ title }}
    </div>
</template>

<script>
export default {
    props: ['title'],
    data() {
        return {
            value: this.title,
        }
    },
    methods: {
       customTitle(e) {
           this.$emit('customTitle', e.target.value)
       }
    }

}
</script>

<style>

</style>