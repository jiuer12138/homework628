<template>
  <input type="text" name="" id="" :value="val" @input="inp" />
</template>

<script>
export default {
  data() {
    return {
      val: '',
    }
  },
  methods: {
    inp(e) {
      return (this.val = e.target.value)
    },
  },
}
</script>

<style></style>
