<template>
    <div>
        <button @click="find_cat()" ref="cat_page">cat button</button>
    </div>
</template>

<script>
import axios from "axios"
import Cookies from "vue-cookies"

    export default {
        methods: {
            find_cat() {
                axios.request({
                    url: `https://aws.random.cat/meow`
                }).then((success)=>{
                    this.$root.$emit(`new_display`, success.data.file);
                    Cookies.set(`selection`, success.data.file)

                    

                }).catch((error)=>{
                    error

                })
            }
        },
        name: 'cat-button'
    }
</script>

<style scoped>

</style>