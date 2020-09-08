<template>
  <c-theme-provider>
    <c-color-mode-provider #default="{ colorMode }">
      <c-box
        :color="colorMode === 'dark' ? 'whiteAlpha.900' : 'gray.700'"
        :bg="colorMode === 'dark' ? 'gray.800' : 'white'"
        transition="all 0.2s ease-in"
      >
        <c-reset />
        <navbar />
        <Nuxt />
      </c-box>
    </c-color-mode-provider>
  </c-theme-provider>
</template>
