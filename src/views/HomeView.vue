<script setup>
import { ref, onMounted } from 'vue';
import Exchanger from '@/components/Exchanger.vue';
import Header from '@/components/Header.vue';
import History from '@/components/History.vue';
import Share from '@/components/Share.vue';
import Slider from '@/components/Slider.vue';
import WhyWe from '@/components/WhyWe.vue';

const isMobile = ref(false);

function checkMobile() {
  isMobile.value = window.innerWidth < 600;
}

onMounted(() => {
  checkMobile();
  window.addEventListener('resize', checkMobile);
});


</script>

<template>
    <header>
      <Header />
    </header>
    <main>
      <Share />
      <template v-if="isMobile">
        <Exchanger />
        <Slider />
      </template>
      <template v-else> 
        <Slider />
        <Exchanger />
      </template>
      <History />
      <WhyWe />
    </main>
</template>

<style lang="scss"></style>
