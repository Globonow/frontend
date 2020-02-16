<template>
  <div id="app">
    <Container>
      <div class="menucontainer">
        <div class="rectangle">
          <table>
            <tr>
              <td>
                <div class="logos"></div>
              </td>
              <td class="hour">20:45</td>
              <td class="programation-name">AVENIDA BRASIL</td>
            </tr>
          </table>
        </div>
      </div>
      <router-view />
    </Container>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.logos {
  position: relative;
  width: 75px;
  height: 75px;
  background-image: url('../assets/avenidaBrasilLogo.jpg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: 140px;
  border-radius: 20px;
  margin-top: 15px;
  margin-left: 40px;
  margin-bottom: 15px;
}

.hour {
  display: block;
  font-size: 20px;
  margin-top: 40px;
  margin-left: 20px;
}

.programation-name {
  font-size: 20px;
  padding-left: 30px;
}
</style>

