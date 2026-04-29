<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <Title>{{ t('label.contact') }}</Title>
  <div class="contact-line">
    <bi-telephone-fill dark:text="white" />
    <Paragraph
      class="contact"
      dark:hover:text="blue-400"
      hover:text="blue-500"
      print:text="no-underline"
      text="underline"
    >
      <a href="tel:+19022038814">(902) 203-8814</a>
    </Paragraph>
  </div>
  <div class="contact-line">
    <bi-envelope-fill dark:text="white" />
    <Paragraph
      class="contact"
      dark:hover:text="blue-400"
      hover:text="blue-500"
      print:text="no-underline"
      text="underline"
    >
      <a href="mailto:maccutler@protonmail.com">maccutler@protonmail.com</a>
    </Paragraph>
  </div>
  <div class="contact-line">
    <bi-github dark:text="white" />
    <Paragraph
      class="contact"
      dark:hover:text="blue-400"
      hover:text="blue-500"
      print:text="no-underline"
      text="underline"
    >
      <a href="https://github.com/mackcutlerdev" target="_blank">mackcutlerdev</a>
    </Paragraph>
  </div>
  <div class="contact-line">
    <bi-linkedin dark:text="white" />
    <Paragraph
      class="contact"
      dark:hover:text="blue-400"
      hover:text="blue-500"
      print:text="no-underline"
      text="underline"
    >
      <a href="https://linkedin.com/in/Mackenzie-Cutler" target="_blank">Mackenzie-Cutler</a>
    </Paragraph>
  </div>
  <div align="items-center" display="hidden" m="y-0 x-auto" print:flex="~">
    <bi-globe2 dark:text="white" />
    <Paragraph
      class="contact"
      dark:hover:text="blue-400"
      hover:text="blue-500"
      print:text="no-underline"
      text="underline"
    >
      <a href="https://mackcutler.com" target="_blank">mackcutler.com</a>
    </Paragraph>
  </div>
</template>

<style scoped>
.contact-line {
  @apply flex my-0 mx-auto items-center;
}
.contact {
  @apply pl-1em m-[0.25em];
}
</style>
