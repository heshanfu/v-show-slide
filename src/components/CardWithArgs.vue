<template>
  <div class="card">
    <div class="card-wrap">
      <div class="card-header">
        <h2 class="card-title">Silver Package</h2><!-- /.card-title -->
      </div><!-- /.card-header -->
      <div class="card-content">
        <p>v-show-slide with duration and easing set</p>
        <ul
          v-show-slide:500:ease-in="featuresOpen"
          class="features">
          <li>Aliquam lorem</li>
          <li>Praesent porttitor nulla vitae posuere</li>
          <li>Suspendisse nisl elit rhoncus</li>
          <li>Donec mi odio faucibus</li>
          <li>Curabitur suscipit suscipit</li>
        </ul><!-- /.features -->
        <button
          @click="toggleFeatures"
          class="toggle-features">{{ featuresOpen ? 'Hide Features' : 'View Features' }}</button><!-- /.toggle-features -->
      </div><!-- /.card-content -->
    </div><!-- /.card-wrap -->
  </div><!-- /.card -->
</template>

<script>
export default {
  name: 'CardWithArgs',
  data () {
    return {
      featuresOpen: false
    }
  },
  methods: {
    toggleFeatures () {
      this.featuresOpen = !this.featuresOpen
    }
  }
}
</script>
