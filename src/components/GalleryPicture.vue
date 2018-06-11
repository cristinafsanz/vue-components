<template>
  <section class="picture">
    <div class="picture__image">
      <img
        :src="data.gifurl"
        class="responsive-image" />
    </div>
    <div class="picture__description">
      <p class="picture__description-text">
        {{ data.title}}
      </p>
      <div class="picture__description-button">
        <button type="button">
          Go
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'GalleryPicture',

  props: {
    data: {
      type: Object,
      required: true
    }
  }
}
</script>

<style>
.picture, .picture__description {
  display: flex;
  flex-direction: column;
}
.picture__image {
  flex-grow: 1;
  display: flex;
  background-color: #f5f5f5;
}
.responsive-image {
  object-fit: cover;
  width: 100%;
  overflow: hidden;
}
.picture__description {
  display: flex;
  flex-direction: column;
  height: 8rem;
  background-color: #e6e6ff;
}
.picture__description-text {
  flex-grow: 1;
  margin-left: 10px;
}
.picture__description-button {
  display: flex;
  justify-content: flex-end;
}
.picture__description-button button {
  margin: 0 10px 10px 0;
  padding: 5px 10px;
  background-color: #ffffff;
}
.picture__description-button button:hover {
  background-color: #854f9b;
  color:#ffffff;
}
</style>
