<script setup lang="ts">
import { Messages } from '../types'
const { t, messages } = useI18n()

const projects = computed(() => (messages.value as Messages)?.en?.projects ?? [])
const projectCount = computed(() => projects.value.length)
const projectUrl = (index: number) => (projects.value[index] as any)?.url
</script>

<template>
  <Title>
    {{ t('label.projects') }}
  </Title>
  <section v-for="index in projectCount" :key="index" m="b-1em">
    <section align="items-center" flex="~" justify="between">
      <SubTitle hover:dark:text="blue-300" hover:text="blue-800">
        <a
          :href="projectUrl(index - 1) || t(`projects[${index - 1}].github`)"
          print:text="!no-underline"
          style="text-decoration: underline"
          target="_blank"
        >
          {{ t(`projects[${index - 1}].name`) }}
        </a>
      </SubTitle>
      <SubTitle>
        <a :href="t(`projects[${index - 1}].github`)" print:display="hidden" target="_blank">
          <bi-github dark:text="white" m="l-1" text="black" />
        </a>
        <a v-if="projectUrl(index - 1)" :href="projectUrl(index - 1)" m="l-1" print:display="hidden" target="_blank">
          <bi-circle-fill m="l-1" text="red-500" />
        </a>
      </SubTitle>
    </section>

    <Headline>
      Made with
      {{ t(`projects[${index - 1}].technologies`) }}
    </Headline>
    <Paragraph v-html="t(`projects[${index - 1}].description`)" />
  </section>
</template>
