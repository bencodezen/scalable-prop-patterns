<template>
  <div class="hello">
    <h1>Scalable Prop Patterns with Vue.js</h1>
    <p>
      For all of the workshop resources,<br />
      check out the
      <a
        href="https://www.github.com/bencodezen/scalable-prop-patterns"
        target="_blank"
        rel="noopener"
        >Scalable Prop Patterns GitHub repository</a
      >.
    </p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    randomNumber: {
      type: Number,
      default: () => Math.floor(Math.random() * 6 + 1)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
  color: #338b64;
}
</style>
