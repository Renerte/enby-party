<template lang="pug">
div.list
  a.list-item(v-for='link in links' v-bind:href="link.url" target="_blank") {{link.label}}
</template>

<script lang="ts">
import axios from 'axios';

export default {
  data() {
    return {
      links: []
    }
  },
  async mounted() {
    let linksReq = await axios.get('https://f002.backblazeb2.com/file/enby-party/links.json');
    this.links = linksReq.data;
  }
}
</script>
