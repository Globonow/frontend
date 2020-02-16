<template>
  <div id="app">
    <Container>
      <div class="menucontainer">
        <div class="column">
          <div class="date dimensions">
            {{ new Date().toLocaleDateString() }}
          </div>
          <div class="list-items">
            <ScheduleItem />
            <ScheduleItem />
            <ScheduleItem />
            <ScheduleItem />
            <ScheduleItem />
            <ScheduleItem />
            <ScheduleItem />
            <ScheduleItem />
            <ScheduleItem />
            <ScheduleItem />
            <ScheduleItem />
            <ScheduleItem />
          </div>
        </div>
        <div class="column">
          <div class="dimensions">EM ESPERA</div>
          <div class="list-items">
            <AwaitingItem />
            <AwaitingItem />
            <AwaitingItem />
          </div>
        </div>

        <div class="column">
          <div class="dimensions">LINHA DO TEMPO</div>
          <TimeLine />
        </div>
      </div>
      <router-view />
    </Container>
  </div>
</template>

<script>
import ScheduleItem from '../components/ScheduleItem.vue';
import AwaitingItem from '../components/AwaitingItem.vue';
import TimeLine from '../components/TimeLine.vue';

export default {
  name: 'app',
  components: {
    ScheduleItem,
    AwaitingItem,
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
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 75px;
  max-height: 75px;
  background-color: #333333;
  text-align: center;
  color: #efefef;
  font-size: 20px;
  padding: auto;
}

.column {
  display: flex;
  flex: 1;
  background: #222222;
  flex-direction: column;
  margin-left: 6px;
  margin-right: 6px;
}

.list-items {
  overflow: scroll;
}
</style>
