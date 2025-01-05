<template>
  <v-app>
    <v-app-bar color="primary">
      <template v-slot:prepend>
        <v-icon aria-hidden="false"> {{ home.icon }} </v-icon>
      </template>
      <template v-slot:title>
        <v-app-bar-title>{{ title }}</v-app-bar-title>
      </template>
    </v-app-bar>
    <v-main>
      <div class="exams">
        <header class="header">
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
        </header>
        <h1>試験一覧</h1>
        <main>
          <ul>
            <li>
              <router-link to="/exams/18">試験1</router-link>
            </li>
            <li>
              <router-link to="/exams/2">試験2</router-link>
            </li>
            <li>
              <router-link to="/exams/3">試験3</router-link>
            </li>
          </ul>
        </main>
        <footer class="footer">
          <p>&copy; 2024 試験プラットフォーム.</p>
        </footer>
      </div>
    </v-main>
  </v-app>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'App',

  data: () => ({
    title: '過去問サイト',
    home: {
      icon: 'mdi-home',
      link: '', //今回は設定しない
    },
  }),
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

/* フッターのスタイル */
.footer {
  background-color: #f4f4f4;
  text-align: center;
  padding: 1rem;
  margin-top: auto;
  font-size: 0.9rem;
  color: #555;
}

.footer p {
  margin: 0;
}

/* メインの試験リスト */
.exams ul {
  list-style: none;
  padding: 0;
}

.exams ul li {
  margin: 0.5rem 0;
}

.exams ul li a {
  text-decoration: none;
  color: #007acc;
}

.exams ul li a:hover {
  text-decoration: underline;
}

/* レスポンシブ対応 */
@media (min-width: 1024px) {
  .exams {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}
</style>
