<script>
export default {
  props: {
    updateLocation: {
      type: Function,
      require: true
    }
  },
  data: () => ({
    location: 'Washington DC'
  }),
  methods: {
    submitUpdate() {
      this.updateLocation(this.location)
    }
  }
}
</script>

<template>
  <div class="map-marker">
    <p>A Map Marker</p>
    <button @click="submitUpdate">Update Location</button>
  </div>
</template>

<style></style>
