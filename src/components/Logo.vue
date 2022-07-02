<script setup lang="ts">
const { t } = useI18n();
</script>

<template>
    <RouterLink class="icon-btn mx-2" to="/" :title="t('button.logo')">
      <img src="./../assets/logo.svg" height="38">
    </RouterLink>
</template>

<style scoped>

</style>
