<template>
  <c-flex
    :color="isDarkMode ? 'whiteAlpha.900' : 'gray.700'"
    :bg="isDarkMode ? 'gray.900' : 'white'"
    transition="all 0.2s ease-in"
    align="center"
    as="nav"
    justify="center"
    shadow="lg"
    py="4"
  >
    <logo width="30" />
    <c-heading mx="5">
      Coffee &lt;b&gt;
    </c-heading>
    <c-text mr="5">
      Home
    </c-text>
    <c-text mr="5">
      Blog
    </c-text>
    <c-text mr="5">
      Featured
    </c-text>
    <c-icon-button :aria-label="isDarkMode ? 'Switch to light mode' : 'Switch to dark mode'" :icon="colorMode === 'light' ? 'moon' : 'sun'" @click="toggleColorMode" />
  </c-flex>
</template>

<script>
export default {
  inject: ['$chakraColorMode', '$toggleColorMode'],
  computed: {
    colorMode: vm => vm.$chakraColorMode(),
    toggleColorMode: vm => vm.$toggleColorMode,
    isDarkMode: vm => vm.colorMode !== 'light'
  }
}
</script>
