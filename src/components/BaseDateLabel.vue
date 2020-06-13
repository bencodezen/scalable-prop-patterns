<script>
export default {
  name: 'BaseDateLabel',
  props: {
    isoDate: {
      /** ISO-8601 format **/
      type: String,
      required: true
    }
  },
  data: () => ({
    /**
     * If numerical, show YYYY-MM-DD (i.e., 2020-06-13)
     * If text, show text version (i.e., June 13, 2020)
     */
    format: 'numerical'
  }),
  computed: {
    date() {
      return new Date(this.isoDate)
    },
    simpleDate() {
      return `${this.yearNumber}-${this.monthNumber}-${this.dayNumber}`
    },
    dayNumber() {
      return this.date.getDate()
    },
    monthNumber() {
      return this.date.getMonth() + 1
    },
    yearNumber() {
      return this.date.getFullYear()
    }
  }
}
</script>

<template>
  <div>
    <p>{{ simpleDate }} ({{ format }})</p>
    <form>
      <label for="numerical-format" name="format-preference">
        <input
          type="radio"
          id="numerical-format"
          value="numerical"
          v-model="format"
        />
        Numerical
      </label>
      <label for="text-format" name="format-preference">
        <input type="radio" id="text-format" value="text" v-model="format" />
        Text
      </label>
    </form>
  </div>
</template>
