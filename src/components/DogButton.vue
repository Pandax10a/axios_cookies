<template>
    <div>
        <button @click="find_dog()" ref="dog_page">dog button</button>
    </div>
</template>

<script>
import axios from "axios"
import Cookies from "vue-cookies"

    export default {
        methods: {
            find_dog() {
                axios.request({
                    url: `https://dog.ceo/api/breeds/image/random`
                }).then((success)=>{
                    this.$root.$emit(`new_display`, success.data.message);
                    Cookies.set(`selection`, success.data.message)

                    console.log(success)
                    success
                    this.$refs.find_dog.insertAdjacentElement(`afterbegin`, `<img src="{success.data.message}">`)

                }).catch((error)=>{
                    error

                })
            }
        },
        name: 'dog-button'
    }
</script>

<style scoped>

</style>