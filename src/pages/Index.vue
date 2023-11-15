<template>
  <q-page style="background-color: hsl(23, 91%, 82%)">
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
    <div class="q-md row" style="padding-top: 10px; padding-bottom: 10px; margin: auto">

      <!-- ENROLL -->
      <div class="q-md col-xs-12 col-sm-6 col-md-6 col-lg-6 text-center" style="padding-bottom: 10px">
        <q-card square dark class="my-card">
          <q-img src="/images/slide1.jpg" :ratio="16 / 12">
            <div class="absolute-center" style="background: rgba(245, 167, 78, 0.8)">
              <p style="font-size: large; font-weight: bold; color: rgb(50, 50, 50)">Шаг к мечте</p>
              <p style="font-size: large; color: rgb(35, 35, 35)">Достаточно лишь захотеть. Мы поможем.</p>

              <p style="font-size: medium; font-weight: bold; text-shadow: 1px rgb(35, 35, 35)">
                <a @click="buyDialog = true">Записаться ></a>
              </p>
            </div>
          </q-img>
        </q-card>
      </div>

      <div class="q-md col-xs-12 col-sm-6 col-md-6 col-lg-6 text-center" style="padding-bottom: 10px">
        <q-card square dark class="my-card">
          <q-img src="/images/menu.jpg" :ratio="16 / 12">
            <div class="absolute-center" style="background: rgba(245, 167, 78, 0.8)">
              <p style="font-size: large; font-weight: bold; color: rgb(50, 50, 50)">Меню</p>
              <p style="font-size: large; color: rgb(35, 35, 35)">Здесь вы можете посмотреть актуальную версию нашего меню</p>

              <p style="font-size: medium; font-weight: bold; text-shadow: 1px rgb(35, 35, 35)">
                <a @click="buyDialog = true">Показать ></a>
              </p>
            </div>
          </q-img>
        </q-card>
      </div>
    </div>


    <!-- INFO -->
    <div class="q-md row flex flex-center" style="padding-bottom: 20px">
      <q-banner rounded class="text-center"
        style="background-color: #f5a74ecc; max-width: 900px; margin: 20px; padding: 15px;">

        <p style="font-size: 20px; font-weight: bold">ул. Абая, дом 2</p>
        <p style="font-size: 18px">
          <a href="" style="color: #3b1b04; font-weight: bold">+7-700-123-4567</a>
        </p>
        <q-chip color="grey-10" :ripple="false" text-color="white" square>
          Пн-Сб: 8.00-21.00, Вск: 10:00-00:00
        </q-chip>
      </q-banner>
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
