<template>
  <div class="hello">
    <h2>{{msg}} {{nam}}</h2>

    <span v-for="opt in options" :key="opt">
      <input type="checkbox" :id="opt.value" :value="opt.value" v-model="checkNames">
      <label for="opt.value">{{opt.value}}</label>
    </span>
    <br>
    {{checkNames}}

    <div>
      <input type="number" v-model="firstNumber"> + <input type="number" v-model="secondNumber"> =
      {{firstNumber + secondNumber}}
    </div>

    <div @mousemove="cordinentX" :style="{backgroundColor: `hsl(${x}, 80%, 50%)`, height: '100px'}">
      {{x}}
    </div>

    <Component1 />
    <Component1 />

    <Test />

  </div>
</template>

<script>
import Component1 from './Component1.vue'
import Test from './Test.vue'

export default {
  components: { Component1, Test },
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      options: [
        {value: 'Tharaka'},
        {value: 'Sam'},
        {value: 'John'},
        {value: 'Larry'}
      ],
      checkNames: [],
      firstNumber: 0,
      secondNumber: 0,
      x: 0
    }
  },
  methods: {
    cordinentX (e) {
      this.x = e.clientX
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
