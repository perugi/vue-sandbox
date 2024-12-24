<script setup>
const msg = '<span style="color: red">Hello World</span>'
const id = 'test'
const isButtonDisabled = ''
const seen = true

const objectOfAttrs = {
  id: 'container',
  class: 'wrapper',
  style: 'background-color: red',
}

const eventName = 'focus'

const eventHandler = () => {
  console.log(`You triggered the ${eventName} event`)
}
</script>

<template>
  <p v-bind="objectOfAttrs">Message: {{ msg.toUpperCase() }}</p>
  <p :id="id + '-test'">message</p>
  <p>Message: <span v-html="msg"></span></p>
  <button :disabled="isButtonDisabled">Button</button>
  <p v-if="seen">Now you see me</p>
  <button @[eventName]="eventHandler">What to do with me</button>
</template>

<style scoped>
#test {
  color: blue;
}

#test-test {
  color: gold;
}
</style>
