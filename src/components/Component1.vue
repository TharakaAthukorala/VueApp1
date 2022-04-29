<template>
  <div class="Component1">
    <div v-for = "t in arry1" :key = "t.id">
      <h3>{{t.title}} Component1 and working in {{t.department}}.</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Component',
  props: ['text'],
  data () {
    return {
      arry1: this.text
    }
  }
}
</script>
