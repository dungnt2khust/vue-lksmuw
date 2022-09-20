<template>
  <input type="text" :value="value" @change="onChange($event)" />
</template>

<script>
export default {
  name: 'Input',
  props: {
    value: {
      type: String,
      default: '',
    },
  },
  methods: {
    onChange(e) {
      console.log(e);
      this.$emit('input', e.target.value);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
