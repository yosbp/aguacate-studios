<template>
  <section class="services box section-padding">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-8 col-md-10">
          <div class="sec-head text-center">
            <h6 class="wow fadeIn font-weight-bold" data-wow-delay=".5s">Nuestros Servicios</h6>
            <h3 class="wow color-font">
              Somos una nueva agencia de desarrollo de productos digitales.
            </h3>
          </div>
        </div>
      </div>
      <div class="row">
        <div v-for="(item, index) in featuresData.slice(0, 3)" class="col-lg-4 wow fadeInLeft mb-3"
          :data-wow-delay="index == 0 ? '.5s' : index == 1 ? '.7s' : '.9s'" :key="item.id">
          <div class="item-box no-curve">
            <span :class="`icon color-font ${item.icon}`"></span>
            <h6>{{ item.title }}</h6>
            <p>{{ item.content }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import featuresData from "@/data/features.json";

const { serviceMB50 } = defineProps(['serviceMB50']);
</script>