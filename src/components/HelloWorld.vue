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
    <h2>Here are my badges:</h2>
    <ul class="badge-list">
      <li v-for="badge in badges" :key="badge.text" class="badge-list-item">
        <BaseBadge
          :type="badge.type"
          :text="badge.text"
          :border-side="badge.borderSide"
        />
      </li>
    </ul>
  </div>
</template>

<script>
import BaseBadge from '@/components/BaseBadge'

export default {
  name: 'HelloWorld',
  components: {
    BaseBadge
  },
  data: () => ({
    badges: [
      { type: 'info', text: 'Info - Left', borderSide: 'left' },
      { type: 'info', text: 'Info - Right', borderSide: 'right' },
      { type: 'info', text: 'Info - Top', borderSide: 'top' },
      { type: 'info', text: 'Info - Bottom', borderSide: 'bottom' },
      { type: 'success', text: 'Success - Left', borderSide: 'left' },
      { type: 'success', text: 'Success - Right', borderSide: 'right' },
      { type: 'success', text: 'Success - Top', borderSide: 'top' },
      { type: 'success', text: 'Success - Bottom', borderSide: 'bottom' },
      { type: 'warning', text: 'Warning - Left', borderSide: 'left' },
      { type: 'warning', text: 'Warning - Right', borderSide: 'right' },
      { type: 'warning', text: 'Warning - Top', borderSide: 'top' },
      { type: 'warning', text: 'Warning - Bottom', borderSide: 'bottom' },
      { type: 'danger', text: 'Danger - Left', borderSide: 'left' },
      { type: 'danger', text: 'Danger - Right', borderSide: 'right' },
      { type: 'danger', text: 'Danger - Top', borderSide: 'top' },
      { type: 'danger', text: 'Danger - Bottom', borderSide: 'bottom' }
    ]
  })
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

.badge-list {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}

.badge-list-item {
  margin-bottom: 1rem;
}
</style>
