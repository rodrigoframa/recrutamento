<template>
  <div>
    <h1>HOME PAGE</h1>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {},
  methods: {
    success () {
      this.$toast.open({
        message: 'Something happened correctly!',
        type: 'is-success'
      })
    }
  }
}
</script>
