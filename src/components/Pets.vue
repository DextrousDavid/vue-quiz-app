<template>
  <div>
    <input type="text" v-model="animalsInput" placeholder="Animal Name..." @keyup.enter="addAnimal()"> 
    <button @click.prevent.stop="addAnimal()">ADD ANIMAL</button>

   <div v-for="animal in animals" :key="animal.id">
     <p> {{ animal.name | capitalize }} </p>
   </div>
   <PlanetList :consoleSomething="consoleSomething"/>
  </div>
</template>

<script>
import PlanetList from './PlanetList'
export default {
  name: 'Pets',
  components: {
    PlanetList,
  },
  data() {
   return {
     name: '',
     animalsInput: '',
     animals: [
       {name: 'Dog'},
       {name: 'Cat'},
       {name: 'Goat'},
       {name: 'Lion'},
     ],
     planets: [
       { name: 'Mercury'},
       { name: 'Venus'},
       { name: 'Earth'},
       { name: 'Mars'},
     ],
   }
  },
  methods: { 
    addAnimal() {
      this.animals.unshift({name: this.animalsInput})
      this.animalsInput = ''
    },
    consoleSomething() {
      console.log('Something consoled!')
  }
  },
  filters: {
    capitalize(value) {
      return value.toUpperCase()
    }
  },
}
</script>

<style scoped>
.blue {
  color: blue;
}
.green {
  border: 2px solid green;
  color: green
}

.red {
  border: 2px solid red;
  color: red
}
</style>
