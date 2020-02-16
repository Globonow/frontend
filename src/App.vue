<template>
  <div id="app">
    <Header />
    <web-admin />
    <!-- <Datepicker /> -->
    <router-view />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import WebAdmin from './pages/WebAdmin.vue';

export default {
  name: 'app',
  components: {
    Header,
    WebAdmin,
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Roboto:400,900&display=swap');
@import '~@/styles/_variables.scss';

*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  outline: 0;
  border: 0;
  box-sizing: border-box;
}

#root,
html,
body {
  height: 100%;
  background-color: $color1;
  color: $color2;
}

#app {
  height: 100%;
}

body {
  -webkit-font-smoothing: antialiased !important;
  text-rendering: optimizeLegibility !important;
}

body,
input,
button {
  font: 14px 'Roboto', sans-serif;
}

*:focus {
  outline: 0;
}

a {
  text-decoration: none;
}

ul {
  list-style: none;
}

button {
  cursor: pointer;
}

input {
  height: 40px;
}
</style>
