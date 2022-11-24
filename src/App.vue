<template>
  <h1>{{ message }}</h1>

  <button @click="reverseMessage">Reverse Message</button>

  <button @click="message += '!'">Append "!"</button>

  <a href="#" @click.prevent="notify">A link with e.preventDefault()</a>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello World!"
    };
  },
  methods: {
    reverseMessage() {
      this.message = this.message.split('').reverse().join('');
    },
    notify() {
      alert("navigation was prevented.");
    },
  },
};
</script>

<style>
button,
a {
  display: block;
  margin-bottom: 1em;
}
</style>
