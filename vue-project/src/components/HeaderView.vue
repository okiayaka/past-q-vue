<template>
  <v-container>
    <div class="header">
      <v-img :src="logo" class="my-3" contain height="200" />
      <nav>
        <ul>
          <li><router-link to="/">home</router-link></li>
          <li><router-link to="/about">about</router-link></li>
          <li><router-link to="/top">top</router-link></li>
          <li><router-link to="/contact">contact</router-link></li>
          <li><router-link to="/login">login</router-link></li>
        </ul>
      </nav>
      <div class="main-visual">
        <h1>〇〇試験一覧</h1>
      </div>
    </div>
  </v-container>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
import logo from '../assets/logo.svg'

export default defineComponent({
  name: 'headerView',
  data() {
    return {
      logo,
    }
  },
})
</script>
<style>
/* ヘッダーのスタイル */
.header {
  background-color: white;
  color: white;
}

.header nav ul {
  list-style: none;
  display: flex;
  gap: 1rem;
  margin: 0;
  padding: 0;
}

.header nav ul li a {
  color: black;
  text-decoration: none;
}

.header nav ul li a:hover {
  text-decoration: underline;
}

.header div {
  text-align: center;
  height: 150px;
  background-color: #007acc;
}
</style>
