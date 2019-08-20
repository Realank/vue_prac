<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div>
      <p v-if="seen">dsfsdfsf</p>
    </div>
    <div>
      <a-button type="primary" @click="buttonClick">Primary</a-button>
      <a-button>Default</a-button>
      <a-button type="dashed">Dashed</a-button>
      <a-button type="danger">Danger</a-button>
      <a-button type="link">Link</a-button>
      <ol>
        <li v-for="todo in todos" :key="todo">
          {{ todo }}
        </li>
      </ol>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import { Button } from 'ant-design-vue'
Vue.use(Button)

export default {
  name: 'HelloWorld',
  props: ['msg'],
  data () {
    return {
      seen: false,
      todos: ['a', 'b', 'c']
    }
  },
  methods: {
    buttonClick () {
      setTimeout(() => {
        this.seen = !this.seen
        this.todos.push('d')
      }, 1000)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
 h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
