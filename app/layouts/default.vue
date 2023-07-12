<template>
  <main :class="[$route.name]" class="main px-4 md:px-0 light">
    <div class="container mx-auto">
      <site-header />
      <nuxt class="nuxt" />
    </div>

    <svg class="divider -mx-4 sm:mx-0" width="100%" viewBox="0 0 10 1">
      <polygon stroke="none" stroke-width="0" fill="#0b3765" points="0,0.6 0,1 10,1 10,0" />
    </svg>

    <site-footer />
  </main>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import SiteHeader from '@/components/partials/header.vue';
import SiteFooter from '@/components/partials/footer.vue';

@Component({
  components: {
    SiteHeader,
    SiteFooter,
  },
})
export default class DefaultLayout extends Vue {}
</script>

<style lang="scss">
.light {
    padding-top: 3rem;
    padding-bottom: 6rem;
    background-image: url(../images/background.svg);
    background-repeat: no-repeat;
    background-position: 50% -700px;
}
.divider {
  position: relative;
  min-width: 100vw;
  margin-top: auto;
}

.nuxt {
  transition: all 0.5s cubic-bezier(0.55, 0, 0.1, 1);
}
</style>
