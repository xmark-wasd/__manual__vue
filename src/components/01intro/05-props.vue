<template>
    <div>
        <h2>props</h2>

        <div
            v-for="(post, index) in posts"
            v-bind:key="index"
        >
            <span>{{post.title}} </span>
            <span> | </span>
            <span>{{post.desc}}</span>
        </div>
    </div>
</template>

<script>
export default {
    props: [
        'posts'
    ],
    data () {
        return {

        }
    }
}
</script>

<style scoped>

</style>