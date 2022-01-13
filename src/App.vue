<template>
  <div>
    <RadioGroup v-model="value" :disabled="disabled">
      <RadioItem value="1">Значение 1</RadioItem>
      <RadioItem value="2">Значение 2</RadioItem>
      <RadioItem value="3">Значение 3</RadioItem>
    </RadioGroup>
    <span>value: {{ value }}</span>
  </div>
</template>

<script>
import RadioGroup from './components/RadioGroup.vue'
import RadioItem from './components/RadioItem.vue'

export default {
  name: 'App',
  components: {
    RadioGroup,
    RadioItem
  },
  data () {
    return {
      value: null,
      disabled: false
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
