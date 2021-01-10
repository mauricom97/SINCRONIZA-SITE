<template>
  <div>
    <div class="fotos-carrosel q-pa-md">
      <q-carousel class="fotos" swipeable animated v-model="slide" thumbnails infinite>
        <q-carousel-slide
          :name="1"
          img-src="https://images.unsplash.com/photo-1448932223592-d1fc686e76ea?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=749&q=80"
        />
        <q-carousel-slide
          :name="2"
          img-src="https://images.unsplash.com/photo-1547394765-185e1e68f34e?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80"
        />
        <q-carousel-slide
          :name="3"
          img-src="https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80"
        />
        <q-carousel-slide
          :name="4"
          img-src="https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&auto=format&fit=crop&w=752&q=80"
        />
      </q-carousel>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 1,
    };
  },
};
</script>

<style>
.fotos{
    border-radius: 10px;
    max-width: 50%;
}
</style>