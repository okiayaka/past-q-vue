<template>
  <div class="home">
    <headerView />
    <h1>ホーム</h1>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

// Components
import headerView from '../components/HeaderView.vue'

export default defineComponent({
  name: 'HomeView',

  components: {
    headerView,
  },
})
</script>
