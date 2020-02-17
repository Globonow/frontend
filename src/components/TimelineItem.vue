<template>
  <div>
    <div class="container">
      <div class="header">
        <font-awesome-icon class="icon" icon="bolt" />
        <div class="edit-image">agora</div>
      </div>
      <div class="description margin-vertical">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Vitae cumque
        temporibus necessitatibus dolor, repellendus aliquam numquam quibusdam
        esse adipisci voluptatum recusandae doloribus possimus, dolore
        provident. Quos consequuntur autem consectetur minus.
      </div>
      <div class="image-container">
        <img class="image" src="../assets/avenidaBrasilLogo.jpg" alt="logo" />
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
.margin-vertical {
  margin-top: 14px;
  margin-bottom: 18px;
}

.container {
  display: flex;
  flex: 1;
  flex-direction: column;
  margin: 18px;
  padding: 24px;
  border-radius: 8px;
  align-items: center;
  justify-content: space-evenly;
  text-align: center;
  background: linear-gradient(#494949, #1e1e1e);
}

.header {
  display: flex;
  width: 100%;
  text-align: left;
  align-items: center;
}

.icon {
  font-size: 18px;
  color: #00ff80;
}

.edit-image {
  font-size: 16px;
  margin-left: 12px;
}

.description {
  font-size: 16px;
  text-align: left;
}

.image {
  width: 100%;
  height: auto;
  border-radius: 8px;
  background-image: url('../assets/avenidaBrasilLogo.jpg');
  background-position: center;
  background-repeat: no-repeat;
}

.hour {
  font-size: 16px;
}

.programation-name {
  font-size: 16px;
}

.iconContainer {
  display: flex;
  flex: 0.2;
  font-size: 18px;
  flex-direction: row;
  align-items: center;
  justify-content: space-evenly;
  text-align: center;
}
</style>
