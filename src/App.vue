<template>
  <h1>{{ count }}</h1>
</template>

<script>
export default {
  data() {
    return {
      count: 2
    }
  },
  beforeCreate() {
    console.log('Before Create!', this.count) // undefined
  },
  created() {
    console.log('Created!', this.count) // 2
  },
  beforeMount() {
    console.log('Before Mount!')
    console.log(document.querySelector('h1')) // null
  },
  mounted() {
    console.log('Mounted!')
    console.log(document.querySelector('h1')) // <h1>2</h1>
  }
}
</script>
