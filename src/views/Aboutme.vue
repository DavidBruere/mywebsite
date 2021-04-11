<template>
  <div class="container">
    <h2 class="headline">Profil Website</h2>
    <div class="row m-5 justify-content-between">
      <div class="col-lg-4">
        <b-card class="card-first-row" fluid title="About me" >
          <div class="card-text">Es freut mich dein Interesse geweckt zu haben. Mein name ist David Bruere und ich bin Frondend Developer.
            Ich wohne in Berlin bin tooootal toll (wie ein tollwuetiger hund).Weiterer Text und blabla</div>
        </b-card>
      </div>
      <div class="col-lg-4">
        <b-img :src="require('../assets/ich.jpg')" thumbnail fluid rounded="circle"
               alt="picture could not load" class="my-image"></b-img>
      </div>
      <div class="col-lg-4">
        <b-card class="card-first-row" border-variant="light" title="short overview">
            <div class="row">
              <b-col>
            <ul class="ul-overview">
              <li>Informatiker</li>
              <li>Web Apps</li>
              <li>Frontend</li>
              <li>Junior</li>
            </ul>
              </b-col>
              <b-col>
            <ul class="ul-overview">
              <li>Vue,js</li>
              <li>Docker</li>
              <li>BootstrapVue</li>
            </ul>
              </b-col>
            </div>
        </b-card>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Aboutme"
}
</script>

<style scoped>
.headline{
  color:white;
  margin-top: 10px;
  text-align: center;
}
.ul-overview{
  text-align: left;
  font-size: 120%;
  padding-left: 8px;
}
.card-first-row {
}
.my-image{
}
.card-text{
  font-size:120%;
}
</style>
