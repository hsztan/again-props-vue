<template>
  <button type="button" @click="onClickAge">Update age</button>
  <p>The user is {{ age }} years old.</p>
</template>

<script>
export default {
  name: 'User',
  props: {
    age: Number
  },
  emits: ['age-change'],
  methods: {
    onClickAge() {
      this.$emit('age-change', 3)
    }
  }
}
</script>