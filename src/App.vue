<template>
  <div id="app">
    <layout>
      <app-form @on-button-clicked='onSubmit'/>
      <div class="list-element" v-for="(element, index) in elements" :key="index">
        <span role="img" aria-label="party">🎉</span> {{element}}
      </div>
    </layout>
  </div>
</template>

<script>
import AppForm from './components/Form.vue';
import Layout from './components/Layout.vue';

export default {
  name: 'app',
  components: {
    AppForm,
    Layout,
  },
  data: function() {
    return {
      elements: []
    }
  },
  methods: {
    onSubmit: function(value) {
      this.elements = [...this.elements, value];
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  margin: 0;
}

.list-element{
  font-size: 30px;
}
</style>
