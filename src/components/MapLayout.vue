<script>
import MapMarker from '@/components/MapMarker'

export default {
  props: {
    updateLocation: {
      type: Function,
      required: true
    }
  },
  components: {
    MapMarker
  },
  data: () => ({
    location: ''
  })
}
</script>

<template>
  <div class="map-layout">
    <h3>Map Layout</h3>
    <MapMarker :update-location="updateLocation" />
  </div>
</template>

<style>
.map-layout {
  border: 5px solid rgb(1, 194, 1);
}
</style>
