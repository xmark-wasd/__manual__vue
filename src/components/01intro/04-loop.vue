<template>
    <div>
        <h2>loop</h2>
        <div
            v-for="(item, index) in items" 
            v-bind:key="index"
        >
            {{item.title}}
        </div>
    </div>
</template>

<script>
export default {
    data () {
        return {
            items: [
                {title: 'one',   desc: 'qwerty 1'},
                {title: 'two',   desc: 'qwerty 2'},
                {title: 'three', desc: 'qwerty 3'},
            ]
        }
    }
}
</script>

<style scoped>

</style>