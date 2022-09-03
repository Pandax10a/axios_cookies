<template>
    <div>
        <img :src="image_url">
    </div>
</template>

<script>

    export default {
        data() {
            return {
                image_url: ""
            }
        },
        methods: {
            show_dog_display(ii) {
                this.image_url = ii
            }
        },
        mounted () {
    this.$root.$on(`new_display`, this.show_dog_display);
},
        name: 'display-selection'
    }
</script>

<style scoped>

</style>