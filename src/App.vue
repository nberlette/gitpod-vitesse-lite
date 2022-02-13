<template>
  <main font-sans p="x-4 y-10" text="center gray-700 dark:gray-200">
    <router-view />
    <Footer />
  </main>
</template>

<style global>
  html, body, #app {
    height: 100%;
    margin: 0;
    padding: 0;
  }

  html.dark {
    background: #121212;
  }
</style>
