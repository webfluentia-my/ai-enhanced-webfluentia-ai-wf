<template>
  <div class="main-wrap">
    <main-header />
    <banner />
    <div class="space-top-short space-bottom-short">
      <v-container>
        <h4 class="use-text-title2 mb-3">
          {{ $t('common.about_team') }}
        </h4>
        <p class="use-text-subtitle2">
          Vestibulum faucibus eget erat eget pretium. Donec commodo convallis eget suscipit orci. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
        </p>
        <team-grid />
      </v-container>
    </div>
    <div class="space-bottom-short">
      <photo-slider />
    </div>
    <call-action />
    <div id="footer">
      <main-footer />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/scss/pages';
</style>

<script>
import brand from '@/assets/text/brand';
import Header from '@/components/Header';
import Banner from '@/components/About/Banner';
import PhotoSlider from '@/components/About/PhotoSlider';
import CallAction from '@/components/CallAction';
import TeamGrid from '@/components/About/TeamGrid';
import Footer from '@/components/Footer';
import { defineNuxtComponent } from '#app';

export default defineNuxtComponent({
  components: {
    'main-header': Header,
    'main-footer': Footer,
    TeamGrid,
    Banner,
    PhotoSlider,
    CallAction,
  },
  head() {
    return {
      title: brand.starter.name + ' - About',
    };
  },
});
</script>
