<template>
    <div>
        <h2>bind attribute with data</h2>
        <input
            v-bind:value="value"
            v-bind:placeholder="placeholder"

            @input="output"

            type="text" 
            name="login" 
        >
        <br>
        <span>{{value}}</span>
    </div>
</template>

<script>
export default {
    data () {
        return {
            value: '',
            placeholder: 'enter your login'
        }
    },
    methods: {
        output (event) {
            this.value += event.data
        }
    }
}
</script>

<style scoped>

</style>