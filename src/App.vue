<template>
    <Props v-bind:posts="posts"></Props>
</template>

<script>
import DeclaredRender from '@/components/01intro/01-declared-render.vue'
import AttributeBind  from '@/components/01intro/02-attribute-bind.vue'
import Condition      from '@/components/01intro/03-condition.vue'
import Loop           from '@/components/01intro/04-loop.vue'
import Props          from '@/components/01intro/05-props.vue'

export default {
    components: {
        DeclaredRender,
        AttributeBind,
        Condition,
        Loop,
        Props
    },
    data () {
        return {
            posts: [
                {title: 'one', desc:   'qwerty 1'},
                {title: 'two', desc:   'qwerty 2'},
                {title: 'three', desc: 'qwerty 3'}
            ]
        }
    }
}
</script>

<style>
* {
    padding: 0;
    margin:  0;
    font-family: sans-serif;
    box-sizing:  border-box;
}
</style>
