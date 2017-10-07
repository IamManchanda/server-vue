<template>
  <div class="grid-container">
    <div class="grid-x grid-margin-x">
      <div class="cell small-12 medium-12">
        <app-header></app-header>
      </div>
      <div class="cell small-12 medium-6">
        <app-server-list></app-server-list>
      </div>
      <div class="cell small-12 medium-6">
        <app-server-details></app-server-details>
      </div>
      <div class="cell small-12 medium-12">
        <app-footer></app-footer>
      </div>
    </div>
  </div>
</template>

<script>
import AppHeader from './components/Shared/AppHeader.vue';
import AppFooter from './components/Shared/AppFooter.vue';
import AppServerList from './components/Server/AppServerList.vue';
import AppServerDetails from './components/Server/AppServerDetails.vue';

export default {
  components: {
    AppHeader, AppServerList, AppServerDetails, AppFooter
  }
}
</script>

<style lang="scss" scoped>
</style>
