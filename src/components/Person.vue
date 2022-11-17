<script lang="ts" setup>
const props = defineProps<{
  name: string,
  description: string
}>()
</script>

<template>
  <div id="person">
    <h1 v-motion-slide-visible-once-right>{{ props.name }}</h1>
    <p v-motion-slide-visible-once-right>{{ props.description }}</p>
  </div>
</template>

<style lang="scss" scoped>
#person {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-size: 5vmin;
  font-weight: 100;
  padding: 0 10vw;

  h1 {
    font-family: 'Roboto Mono', monospace;
  }

  p {
    margin-bottom: 20px;
  }
}
</style>
