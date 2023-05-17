<script setup lang="ts">
import { createIntl } from '@formatjs/intl'
import { provideIntl } from 'vue-intl';
import HelloWorld from './components/HelloWorld.vue';

provideIntl(
  createIntl({
    locale: 'en',
    defaultLocale: 'en',
    messages: {
      'Patrick said "I love this game"': "🤷‍♂️",
    },
  })
)
</script>

<template>
  <HelloWorld />
</template>
