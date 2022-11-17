<template>
    <div>
        <h2>declared render</h2>
        <p>plus:  <span>{{plus}}</span></p>
        <p>minus: <span>{{minus}}</span></p>
        <button @click="addPlus">+</button>
        <button @click="addMinus">-</button>
    </div>
</template>

<script>
export default {
    data () {
        return {
            plus:  0,
            minus: 0
        }
    },
    methods: {
        addPlus () {
            this.plus++
        },
        addMinus () {
            this.minus++
        }
    }
}
</script>

<style scoped>

</style>