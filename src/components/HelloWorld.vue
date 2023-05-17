<script setup lang="ts">
import { useIntl } from 'vue-intl'

const intl = useIntl()

const drI18n = (descriptor: { defaultMessage: string, description?: { tags: string } }, values?: Record<string, string | number | boolean | null | undefined | Date>): string => {
  return intl.formatMessage({ ...descriptor, id: descriptor.defaultMessage }, values)
}

const scriptTranslatedString = drI18n({
  defaultMessage: 'In script translated string'
})
</script>

<template>
  {{ drI18n({
    defaultMessage: 'Hello',
    description: {
      tags: 'rainbow, kittens'
    }
  }) }}<br />

  {{ drI18n({
    defaultMessage: 'Hello',
    description: {
      tags: 'test'
    }
  }) }}<br />

  {{ drI18n({
    defaultMessage: "My name is {name}"
  }, {
    name: "Michel"
  }) }}<br />

  {{ drI18n({
    defaultMessage: 'Patrick said "I love this game"'
  }) }}<br />

  {{ drI18n({
    defaultMessage: "Will.I.Am"
  }) }}<br />

  {{ scriptTranslatedString }}
</template>
