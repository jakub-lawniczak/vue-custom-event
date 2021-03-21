<template>
    <div class="">
        <h2>{{ title }}</h2>
        <button @click="changeTitle">Change Title</button>
    </div>
  
</template>

<script>
export default {
    props: ['title'],
    data() {
        return {
            // title: 'Hello Worlds'

        }
    },
    methods: {
        changeTitle: function() {
            this.$emit('changeTitle', 'Hello Vue ninja')
        }
    }
}
</script>

<style>

</style>