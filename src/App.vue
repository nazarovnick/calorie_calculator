<template>
  <div id="panel">
    <app-button sex="male" :type="maleActive" @action="active = 'male'"></app-button>
    <app-button sex="female" :type="femaleActive" @action="active = 'female'"></app-button>
  </div>
</template>

<script>
import AppButton from '@/AppButton'

export default {
  data () {
    return {
      active: 'male'
    }
  },
  methods: {
  },
  computed: {
    maleActive () {
      return this.active === 'male' ? 'active' : ''
    },
    femaleActive () {
      return this.active === 'female' ? 'active' : ''
    }
  },
  components: {
    'app-button': AppButton
  }
}
</script>

<style>
</style>
