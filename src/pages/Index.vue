<template>
  <q-page style="background-color: hsl(0, 0%, 100%)">
    <!-- CAROUSEL -->
    <div class="q-md">
      <q-carousel animated v-model="slide" class="carousel" :class="{ 'full-height': isFullHeight }" arrows navigation
        infinite :autoplay="autoplay" @mouseenter="autoplay = false" @mouseleave="autoplay = true">

        <q-carousel-slide :name="1" img-src="/images/slide1.jpg" />
        <q-carousel-slide :name="2" img-src="/images/slide2.jpg" />
        <q-carousel-slide :name="3" img-src="/images/slide3.jpg" />
      </q-carousel>
    </div>


    <!-- CONTENT -->
    <div class="q-md row" style="margin: auto">

      <!-- ENROLL -->
      <div class="q-md col-xs-12 col-sm-6 col-md-6 col-lg-6 text-center" style="padding: 10px">
        <q-card square dark class="my-card">
          <q-img src="/images/slide1.jpg" :ratio="16 / 12">
            <div class="absolute-center" style="background: rgba(33, 33, 33, 0.8)">
              <p style="font-size: large; font-weight: bold">{{ $t("content.title1") }}</p>
              <p style="font-size: large">{{ $t("content.text1") }}</p>

              <p style="font-size: medium; font-weight: bold; text-shadow: 1px rgb(35, 35, 35)">
                <q-btn href="/about" outline rounded color="white" :label="$t('content.show1')" />
              </p>
            </div>
          </q-img>
        </q-card>
      </div>

      <div class="q-md col-xs-12 col-sm-6 col-md-6 col-lg-6 text-center" style="padding: 10px">
        <q-card dark class="my-card">
          <q-img src="/images/menu.jpg" :ratio="16 / 12">
            <div class="absolute-center" style="background: rgba(33, 33, 33, 0.8)">
              <p style="font-size: large; font-weight: bold">{{ $t("content.title2") }}</p>
              <p style="font-size: large">{{ $t("content.text2") }}</p>

              <p style="font-size: medium; font-weight: bold; text-shadow: 1px rgb(35, 35, 35)">
                <q-btn outline rounded color="white" :label="$t('content.show2')" />
              </p>
            </div>
          </q-img>
        </q-card>
      </div>
    </div>


    <!-- INFO -->
    <q-container>
      <q-card square
        style="border-radius: 10px; overflow: hidden; background: linear-gradient(to bottom, #FFFFFF, #FFFFFF)">
        <q-card-section style="text-align: center; padding: 0px">
          <h2 style="font-size: 40px">{{ $t("location.title") }}</h2>
        </q-card-section>

        <q-card-section style="text-align: center; padding: 30px; padding-top: 0px">
          <div class="map-frame">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2906.8932537808346!2d76.86659347608303!3d43.23269767112514!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x388369a87d5f7551%3A0x8e70b7a65d73f497!2sAbay%20Ave%202%2C%20Almaty%20050000!5e0!3m2!1sen!2skz!4v1700214471126!5m2!1sen!2skz"
              width="100%" height="300" style="border:0;" allowfullscreen="" loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"></iframe>
          </div>
        </q-card-section>
      </q-card>
    </q-container>
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

<style scoped>
.map-frame {
  max-width: 400px;
  margin: 0 auto;
  border-style: solid;
  border-width: 4px 4px 4px 4px;
  border-color: black;
}
</style>
