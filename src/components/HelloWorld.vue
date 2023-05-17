<script setup lang="ts">
import { useIntl } from 'vue-intl'

const intl = useIntl()
</script>

<template>
  {{ intl.formatMessage({
    id: 'Hello World',
    defaultMessage: 'This is hello world',
    description: {
      whatever: 1,
      tags: 'rainbow, kittens',
      otherMeta: 'why not'
    }
  }) }}
</template>
