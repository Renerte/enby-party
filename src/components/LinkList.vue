<template lang="pug">
div.list
  a.list-item(v-for='link in links' v-bind:href="link.url" rel="noreferrer" target="_blank") {{link.label}}
</template>

<script lang="ts">
import links from '../links.json';

export default {
  data() {
    return {
      links
    }
  }
}
</script>
