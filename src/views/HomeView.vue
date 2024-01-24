<template>
  <RestoranteHeader />
  <RestauranteSlider :arreglo="arreglo" />

</template>

<script>
import 'vue3-carousel/dist/carousel.css'

// @ is an alias to /src
import RestoranteHeader from '@/components/RestoranteHeader.vue'
import RestauranteSlider from '@/components/RestauranteSlider.vue'

export default {
  name: 'HomeView',
  components:{ 
    RestoranteHeader,
    RestauranteSlider
  },data() {
    return {
      arreglo: [
        'hola uno',
        'hola dos',
    ]
    }
  }

}
</script>
<style>
body {
  height: 100%;
  width: 100%;
  background-color: #444 !important;
}
</style>
```
