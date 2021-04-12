<template>
  <div class="container-fluid">
    <h2 class="headline">Profil Website</h2>
    <div class="row m-5 justify-content-between">
      <div class="col-lg-4 mb-3">
        <b-card class="card-first-row" fluid align="center" title="About me">
          <div class="card-text">Es freut mich dein Interesse geweckt zu haben. Mein name ist David Bruere und ich bin
            Frondend Developer.<br>
            Ich wohne in Berlin bin tooootal toll (wie ein tollwuetiger hund).Weiterer Text und blabla
          </div>
        </b-card>
      </div>
      <div class="col-lg-4 mb-3">
        <b-img :src="require('../assets/ich.jpg')" thumbnail fluid rounded="circle"
               alt="picture could not load" class="my-image"></b-img>
      </div>
      <div class="col-lg-4 mb-3">
        <b-card class="card-first-row" align="center" title="short overview">
          <div class="row">
            <b-col>
              <ul class="ul-overview">
                <li>Fachinformatiker</li>
                <li>Web Anwendungen</li>
                <li>Frontend Developer</li>
                <li>Junior (1 Jahr)</li>
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
    <div class="row">
      <div class="col-lg-12">
        <b-button v-b-toggle.collapse-1 class="btn-light ml-5 mt-3 mb-0">Visit Projekts</b-button>
        <hr size="25" width="95%" color="white">
        <b-collapse id="collapse-1">
          <div class="row">
            <div class="col-lg-3" v-for="project in projects" :key="project.id">
              <b-card class="mb-3 rounded-1" :title=project.title
                      :img-src="require('../assets/projectpictures/'+project.imagepath)"
                       img-height="200" img-width="200">
                <b-card-text class="card-text-short">{{ project.description }}</b-card-text>
              </b-card>
            </div>
          </div>
        </b-collapse>
      </div>
    </div>


    <b-button v-b-toggle.collapse-2 class="btn-light ml-5 mt-3">Visit Skills</b-button>
    <hr size="25" width="95%" color="white">

    <b-collapse id="collapse-2">

    </b-collapse>


  </div>
</template>

<script>

import projects from "../data/projects.js"

export default {
  name: "Aboutme",

  data() {
    return {
      projects: projects
    }
  }
}

</script>

<style scoped>
.headline {
  color: white;
  margin-top: 10px;
  text-align: center;
}

.ul-overview {
  text-align: left;
  font-size: 130%;
}

.btn-light {
  box-shadow: none !important;
}

.card-text {
  font-size: 130%;
  text-align: left;
}
.card-text-short {
  display: -webkit-box;
  max-width: 100%;
  -webkit-line-clamp: 5;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

</style>
