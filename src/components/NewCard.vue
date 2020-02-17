<template>
  <div>
    <div class="container">
      <div class="header">
        <font-awesome-icon class="icon" icon="image" />
        <!-- <div class="edit-image">Adicionar Imagem</div> -->
        <!-- <label for="img">Select image:</label> -->
        <input
          class="edit-image"
          type="file"
          @change="onFileSelected"
          accept="image/*"
        />
      </div>
      <input
        class="edit-image"
        type="time"
        @change="onTimeSelected"
        accept="image/*"
      />
      <div class="description margin-vertical">
        <textarea name="" id="text-card" cols="105" rows="6"></textarea>
      </div>
      <div class="image-container">
        <!-- <img class="image" src="../assets/avenidaBrasilLogo.jpg" alt="logo" /> -->
        <div class="button-container">
          <div class="send-button">ADICIONAR</div>
        </div>
      </div>
    </div>
    <router-view />
  </div>
</template>

<script>
import Vue from 'vue';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

Vue.component('font-awesome-icon', FontAwesomeIcon);

export default {
  name: 'NewCard',
  data() {
    return {
      selectedFile: null,
    };
  },
  methods: {
    onFileSelected(event) {
      this.selectedFile = event.target.files[0];
    },
    onTimeSelected() {},
  },
};
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
  /* align-items: center; */
  justify-content: center;
}

textarea {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;

  width: 100%;
  font-size: 16px;
  padding: 12px;
}

.button-container {
  margin: 0 auto;
  padding-top: 8px;
  padding-bottom: 8px;
  background: linear-gradient(#494949, #1e1e1e);
  border-radius: 28px;
  border: 1px solid #00ff80;
  width: 160px;
}

.send-button {
  font-size: 18px;
  color: #00ff80;
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
  margin-bottom: 14px;
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
