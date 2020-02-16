<template>
  <div id="app">
    <Container>
      <div class="menucontainer">
        <div class="column">
          <div class="date dimensions">{{ new Date() }}</div>
          <List />
        </div>
        <div class="column">
          <div class="on-wait dimensions">EM ESPERA</div>
        </div>

        <div class="column">
          <div class="timeline dimensions">LINHA DO TEMPO</div>
          <TimeLine />
        </div>
      </div>
      <router-view />
    </Container>
  </div>
</template>

<script>
import List from '../components/List.vue';
import TimeLine from '../components/TimeLine.vue';

export default {
  name: 'app',
  components: {
    List,
    TimeLine,
  },
};
</script>

<style scoped>
.menucontainer {
  display: flex;
  flex: 1;
  flex-direction: row;
  background: linear-gradient(#494949, #1e1e1e);
}

.dimensions {
  height: 96px;
  background-color: #333333;
  text-align: center;
  color: #efefef;
  font-size: 1.8vw;
  padding: 30px;
}

.column {
  display: flex;
  flex: 1;
  flex-direction: column;
  margin-left: 6px;
  margin-right: 6px;
}
</style>