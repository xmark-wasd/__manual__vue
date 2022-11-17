<template>
    <div>
        <h2>condition render</h2>
        <div v-if="toggle === true">
            <span> on </span>
        </div>
        <div v-else>
            <span> off </span>
        </div>
        <button @click="toggleHandler">on / off</button>
    </div>
</template>

<script>
export default {
    data () {
        return {
            toggle: false
        }
    },
    methods: {
        toggleHandler () {
            this.toggle
                ? this.toggle = false 
                : this.toggle = true
        }
    }
}
</script>

<style scoped>

</style>