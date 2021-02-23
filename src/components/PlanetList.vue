<template>
  <div>
      <p v-for="planet in planets" :key="planet.id">
          {{ planet.name | capitalize }}
      </p>

      <button @click="consoleSomething()">Console Something</button>
  </div>
</template>

<script>
export default {
    props: ['consoleSomething'],
    filters: {
    capitalize(value) {
      return value.toUpperCase()
    }
  },
}
</script>

<style>

</style>