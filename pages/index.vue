<template>
  <div>
    <h1>Hola {{ nombre }}</h1>
    <input type="text" v-model="nombre">
    tienes {{ cuenta }} puntos
    el doble sería {{ calculaDoble }}
    <button @click="suma">Sumar puntos</button>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data () {
    return {
      cuenta: 0,
      nombre: 'Mundo'
    }
  },
  methods: {
    suma () {
      this.cuenta++
    }
  },
  computed: {
    calculaDoble () {
      return this.cuenta * 2
    }
  }
}
</script>

<style scoped>
h1 {
  color:red;
}
</style>
