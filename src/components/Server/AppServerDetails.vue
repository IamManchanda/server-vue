<template>
  <div>
    <div v-if="!server">
      <p>Please select a server first.</p>
    </div>
    <div v-else>
      <p>Server #{{ server.id }} selected, Status: <strong> {{ server.status }} </strong> </p>
      <button class="button primary small rounded" @click="resetStatus">Change to normal</button>
    </div>
  </div>
</template>

<script>
  import { serverBus } from '../../main';

  export default {
    data() {
      return {
        server: null
      };
    },
    methods: {
      resetStatus() {
        this.server.status = 'Normal';
      }
    },
    created() {
      serverBus.$on('serverSelected', (server) => {
        this.server = server;
      });
    }
  }
</script>

<style lang="scss" scoped>
</style>