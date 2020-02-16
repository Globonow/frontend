<template>
  <div>
    <div class="container">
      <div class="infos-container">
        <img
          class="logos margin-horizontal"
          src="../assets/avenidaBrasilLogo.jpg"
          alt="logo"
        />
        <div class="hour margin-horizontal">20:45</div>
        <div class="programation-name margin-horizontal">AVENIDA BRASIL</div>
      </div>
      <div class="icon-container">
        <font-awesome-icon class="icon" icon="chevron-right" />
      </div>
    </div>
    <router-view />
  </div>
</template>

<script>
import Vue from 'vue';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

Vue.component('font-awesome-icon', FontAwesomeIcon);

export default {};
</script>

<style scoped>
.margin-horizontal {
  margin-left: 10px;
  margin-right: 10px;
}

.container {
  display: flex;
  flex: 1;
  flex-direction: row;
  align-items: center;
  justify-content: space-evenly;
  text-align: center;
  background: linear-gradient(#494949, #1e1e1e);
}

.infos-container {
  display: flex;
  flex: 0.8;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  text-align: center;
}

.logos {
  width: 50px;
  height: 50px;
  background-image: url('../assets/avenidaBrasilLogo.jpg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: 140px;
  border-radius: 8px;
  margin-top: 15px;
  margin-left: 40px;
  margin-bottom: 15px;
}

.hour {
  font-size: 16px;
}

.programation-name {
  font-size: 16px;
}

.icon-container {
  display: flex;
  flex: 0.2;
  font-size: 18px;
  flex-direction: row;
  align-items: center;
  justify-content: space-evenly;
  text-align: center;
}

.icon {
  color: #efefef;
}
</style>
