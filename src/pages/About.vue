<template>
  <q-page style="background-color: hsl(0, 0%, 100%)">

    <div class="article-content">

      <div class="image-container">
        <img src="/images/slide1.jpg" class="rounded-image" />
      </div>

      <div class="article-text">
        <h1 style="margin-top: 10px">{{ $t("about.title") }}</h1>
        <p style="font-size: 30px">{{ $t("about.text") }}</p>
      </div>

    </div>

  </q-page>
</template>

<script>
import { defineComponent, ref } from 'vue'
import { useQuasar } from 'quasar'

export default defineComponent({
  name: 'About',

  setup() {
    const $q = useQuasar()

    return {

    }
  }
})
</script>

<style scoped>
.article-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin-top: 30px;
}

.image-container {
  max-width: 600px;
  margin-bottom: 20px;
}

.rounded-image {
  border-radius: 10px;
  max-width: 100%;
  height: auto;
}

.article-text {
  max-width: 800px;
}
</style>
