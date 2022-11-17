# Введение

Краткое описание основных возможностей vue

---

## оглавление

- [декларативная отрисовка]()
- [двухстороннее связывание]()
- [условная отрисовка]()
- [отрисовка в цикле]()
- [Свойства компонента]()

---

# Декларативная отрисовка

```ts
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
```

---

# двухстороннее связывание

```ts
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
```

---

# условная отрисовка

```ts
<template>
    <div>
        <h2>condition render</h2>
        <div v-if="toggle">
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
```

---

# отрисовка в цикле

```ts
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
```

---

# Свойства компонента

__Родительский компонент:__
```ts
<template>
    <Props v-bind:posts="posts"></Props>
</template>

export default {
    components: {
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

```

__дочерний компонент:__

```ts
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
```

---