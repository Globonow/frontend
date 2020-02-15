<template>
  <div id="app">
    <Container>
      <Header></Header>
      <div class="menucontainer">
        <div class="date dimensions">{{ new Date() }}</div>
        <div class="dividers"></div>
        <div class="on-wait dimensions">EM ESPERA</div>
        <div class="dividers"></div>
        <div class="timeline dimensions">LINHA DO TEMPO</div>
      </div>
      <router-view />
    </Container>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.menucontainer {
  display: flex;
}

.dimensions {
  height: 96px;
  width: 32.98%;
  background-color: #333333;
  text-align: center;
  color: #efefef;
  font-size: 1.8vw;
  padding: 30px;
}

.dividers {
  height: 822px;
  width: 0.5%;
  background: linear-gradient(#494949, #1e1e1e);
  display: flex;
}
</style>
