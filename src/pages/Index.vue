<template>
  <q-page style="background-color: #FFFFFF">
    <!-- CAROUSEL -->
    <div class="q-md">
      <q-carousel animated v-model="slide" class="carousel" :class="{ 'full-height': isFullHeight }" arrows navigation
        infinite :autoplay="autoplay" @mouseenter="autoplay = false" @mouseleave="autoplay = true">

        <q-carousel-slide :name="1" img-src="/images/slide1.jpg" />
        <q-carousel-slide :name="2" img-src="/images/slide2.jpeg" />
        <q-carousel-slide :name="3" img-src="/images/slide3.jpg" />
      </q-carousel>
    </div>

  </q-page>
</template>

<script>
import { defineComponent, ref } from 'vue'
import { useQuasar } from 'quasar'

export default defineComponent({
  name: 'Index',

  setup() {
    const $q = useQuasar()

    return {
      slide: ref(1),
      autoplay: ref(true),
      isFullHeight: ref(),
    }
  }
})
</script>
