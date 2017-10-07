<template>
  <ul class="list-group">
    <app-server v-for="server in servers" :server="server"></app-server>
  </ul>
</template>

<script>
  import AppServer from './AppServer.vue';

  export default {
    data() {
      return {
        servers: [
          { id: 1, status: 'Unknown' },
          { id: 2, status: 'Critical' },
          { id: 3, status: 'Unknown' },
          { id: 4, status: 'Critical' }
        ]
      };
    },
    components: { AppServer }
  }
</script>

<style lang="scss" scoped>
</style>