<template>
  <div class="form">
    <input class="input" v-model="value" placeholder="Enter name"/>
    <button @click="onClick">Submit!</button>
  </div>
</template>

<script>
export default {
  name: 'AppForm',
  props: {
  },
  data: function() {
    return {
      value: ''
    }
  },
  methods: {
    onClick: function() {
      this.$emit('on-button-clicked', this.value);
      this.value = '';
    }
  }
}
</script>

<style scoped>
.input {
  height: 30px;
  width: 200px;
  font-size: 20px;
}

.form {
   margin: 40px;
}
</style>
