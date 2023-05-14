<template>
  <div class="btn" :class="type" @click="$emit('action')">
    <img :class="getClass" :src="require('./img/' + getIcon)" alt="">
  </div>
</template>

<script>
export default {
  emits: ['action'],
  props: {
    type: String,
    sex: String
  },
  mounted () {
    console.log(this.sex)
  },
  data () {
    return {
    }
  },
  computed: {
    getIcon () {
      return this.sex === 'female' ? 'femaleicon.png' : 'maleicon.png'
    },
    getClass () {
      return this.sex === 'female' ? 'female' : 'male'
    }
  }
}
</script>

<style scoped>

</style>
