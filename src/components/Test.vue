<template>
  <div class="Test">
    hello

    <Component1 :text = this.arry />
  </div>
</template>

<script>
import Component1 from './Component1.vue'
export default {
  components: { Component1 },
  name: 'Test',
  data () {
    return {
      arry: [
        {id: 1, title: 'SE', department: 'Devops'},
        {id: 2, title: 'SSE', department: 'Enterprise'},
        {id: 3, title: 'ASE', department: 'Open Sourse'},
        {id: 4, title: 'SE', department: 'Intergration'},
        {id: 5, title: 'SSE', department: 'ALGe'}
      ]
    }
  }
}
</script>

<style>

</style>
