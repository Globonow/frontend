<template>
  <container>
    <Header>
      <FunctionalCalendar
        v-model="calendarData"
        v-on:changedMonth="changedMonth"
        v-on:changedYear="changedYear"
        :sundayStart="true"
        :date-format="'dd/mm/yyyy'"
        :is-date-range="true"
        :is-date-picker="true"
      ></FunctionalCalendar>
    </Header>
  </container>
</template>

<script>
import Vue from 'vue';
import FunctionalCalendar from 'vue-functional-calendar';
Vue.use(FunctionalCalendar, {
  dayNames: ['Seg', 'Ter', 'Qua', 'Qui', 'Sex', 'Sab', 'Dom'],
});

export default {
  components: {
    FunctionalCalendar,
  },
  data() {
    return {
      calendarData: {},
      calendarConfigs: {
        sundayStart: true,
        dateFormat: 'dd/mm/yyyy',
        isDatePicker: true,
        isDateRange: false,
        isDark: true,
        isAutoCloseable: true,
      },
    };
  },
};
</script>

<style scoped>
.logo {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 30%;
  padding: 30px;
}
</style>
