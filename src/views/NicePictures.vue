<template>
  <div class="pictures">
    <header class="pictures__header">
      <span>ACME Ltd.</span>
      <span>Welcome John</span>
    </header>
    <main class="pictures__main">
      <h1>{{ title }}</h1>
      <article class="pictures__main-container">
        <gallery-picture
          v-for="(data, index) in gifs"
          :key="index"
          :data="data"
          class="pictures__gallery-picture">
        </gallery-picture>
      </article>
    </main>
    <footer class="pictures__footer">
      <span>{{ users }} users active</span>
    </footer>
  </div>
</template>

<script>
import json from '../json/gifs.json'
import GalleryPicture from '@/components/GalleryPicture'

export default {
  name: 'NicePictures',

  components: {
    GalleryPicture
  },

  data () {
    return {
      title: 'Nice pictures',
      users: 8,
      gifs: json
    }
  }
}
</script>

<style>
.pictures {
  display: flex;
  flex-direction: column;
  height: 100vh;
}
.pictures__header, .pictures__footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-shrink: 0;
  height: 2rem;
  padding: 1rem 2rem;
  background-color: #854f9b;
  color: #ffffff;
}
.pictures__main {
  flex-grow: 1;
  overflow: auto;
  padding: 2rem;
}
.pictures__main-container {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: space-around;
}
.pictures__gallery-picture {
  width: 100%;
}
@media (min-width: 768px) {
  .pictures__gallery-picture {
    width: calc(50% - 24px);
    padding: 12px;
  }
}
@media (min-width: 1024px) {
  .pictures__gallery-picture {
    width: calc(33% - 24px);
    padding: 12px;
  }
}
</style>
