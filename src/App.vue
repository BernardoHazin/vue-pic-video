<template>
  <div id="app">
    <label for="img" @click="$refs.input.click()">
      <slot></slot>
    </label>
    <input type="file" ref="input" :accept="accept" @change="change" name="img" style="display: none;">
  </div>
</template>

<script>
export default {
  props: {
    accept: {
      type: String
    }
  },
  methods: {
    change () {
      this.$emit('value', this.$refs.input.files[0])
      const reader = new FileReader()
      reader.onload = (e) => {
        this.$emit('preview', e.target.result)
      }
      reader.readAsDataURL(this.$refs.input.files[0])
    }
  }
}
</script>