<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import testimonios from "../../assets/jsons/testimonios.json";

// Importar estilos de Swiper
import "swiper/css";
import "swiper/css/effect-fade";
import "swiper/css/navigation";
import "swiper/css/pagination";

// Importar módulos requeridos
import { EffectFade, Navigation, Pagination } from "swiper/modules";

// Definir los módulos que usará Swiper
const modules = [EffectFade, Navigation, Pagination];
</script>

<template>
  <div class="container_swiper fl-column" id="testimonios">
    <h2>Testimonios</h2>
    <Swiper
      :spaceBetween="50"
      :modules="modules"
      :slides-per-view="1"
      :navigation="true"
      :pagination="{ dynamicBullets: true }"
      :loop="true"
      class="my-swiper"
    >
      <SwiperSlide
        class="fl-column"
        v-for="testimonio in testimonios"
        :key="testimonio.id"
      >
        <p>
          {{ testimonio.testimonio }}
        </p>

        <h5>{{ testimonio.nombre }}</h5>
      </SwiperSlide>
    </Swiper>
  </div>
</template>

<style scoped>
.container_swiper {
  width: 100%;
  height: 400px;
  padding-inline: 10%;
  margin-block: calc(var(--space) * 2);
  background: var(--secondaryColorLight);
}
.fl-column {
  gap: 0px !important;
}
h2 {
  width: 100%;
  background: #fff;
  text-align: center;
  padding-top: var(--space);
}
.swiper {
  background: #fff;
  width: 100%;
  height: 100%;
  padding-inline: calc(var(--space) * 3);
}

.swiper-slide {
  width: 100% !important;
  background-position: center;
  background-size: cover;
}

.swiper-slide p {
  width: 60%;
  margin-inline: auto;
  text-align: center;
  margin-top: calc(var(--space) * 5);
}
.swiper-slide h5 {
  text-align: center;
  margin-top: calc(var(--space) * 3);
  font-weight: 500;
  text-transform: uppercase;
}
.swiper-slide img {
  display: block;
  width: 100%;
}

@media screen and (max-width: 800px) {
  .swiper-slide p {
    width: 100%;
    text-align: inherit;
    margin-top: calc(var(--space) * 3);
  }
}
</style>
