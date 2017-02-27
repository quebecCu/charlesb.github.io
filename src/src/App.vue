<template>
  <div id="app" class="fullHeight">
    <div class="container-fluid fullHeight">
      <div class="row fullHeight">
        <div class="hidden-xs col-md-3 bg-info fullHeight">
          <h1 class="text-center">Charles Belzile</h1>
          <p class="text-center">&Eacute;tudiant en informatique originaire du Qu&eacute;bec. Pr&eacute;sentement en France.</p>
          <hr style="color:black;background-color:black;">
          <ul class="nav nav-pills nav-stacked">
            <li v-bind:class="{ active: currentView === 'accueil' }" @click="currentView = 'accueil'"><a href="#">Accueil</a></li>
            <li v-bind:class="{ active: currentView === 'competences' }" @click="currentView = 'competences'"><a href="#">Comp&eacute;tences informatique</a></li>
            <li v-bind:class="{ active: currentView === 'experiences' }" @click="currentView = 'experiences'"><a href="#">Exp&eacute;riences professionelles</a></li>
            <li v-bind:class="{ active: currentView === 'scolaires' }" @click="currentView = 'scolaires'"><a href="#">Parcours scolaire</a></li>
            <li v-bind:class="{ active: currentView === 'loisirs' }" @click="currentView = 'loisirs'"><a href="#">Loisirs</a></li>
          </ul>
          <div class="menu-bottom">
            <div class="centerd">
              <div class="dropup">
                <button class="btn btn-default dropdown-toggle" type="button" id="dropdownMenu1" @click="toggleLang" @blur="toggleLang">
                  FR - Langue maternelle
                  <span class="caret"></span>
                </button>
                <ul id="showLang" class="dropdown-menu">
                  <li><a href="#">EN - Fluent</a></li>
                  <li class="disabled"><a href="#">DE - Derzeit lernen</a></li>
                  <li class="disabled"><a href="#">ES - Actualmente aprendiendo</a></li>
                </ul>
              </div>
              <br>
              <p>
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x "></i>
                  <i class="fa fa-envelope fa-stack-1x" style="color:#d9edf7;"></i>
                </span>
                <span class="fa-stack fa-lg">
                  <i class="fa fa-github fa-stack-2x"></i>
                </span>
              </p>
            </div>
          </div>
        </div>
        <div class="col-xs-12 col-md-9 text-center maxHeight">
          <keep-alive>
            <transition name="component-fade" mode="out-in">
              <component :is="currentView" class="maxHeight">
                <!-- inactive components will be cached! -->
              </component>
            </transition>
          </keep-alive>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Accueil from './Components/Accueil.vue'
import Competences from './Components/Competences.vue'
import Experiences from './Components/Experiences.vue'
import Scolaires from './Components/Scolaires.vue'
import Loisirs from './Components/Loisirs.vue'

export default {
  name: 'app',
  components:{
    accueil: Accueil,
    competences: Competences,
    experiences: Experiences,
    scolaires: Scolaires,
    loisirs: Loisirs
  },
  data () {
    return {
      showLang: false,
      currentView: 'accueil'
    }
  },
  methods:{
    toggleLang: function(){
      if (this.showLang === false){
        document.getElementById('showLang').style.display = 'block';
        this.showLang = true;
      }else{
        document.getElementById('showLang').style.display = 'none';
        this.showLang = false;
      }
    }
  }
}
</script>

<style>
.menu-bottom{
  position: absolute;
  display:table;
  vertical-align:middle;
  bottom:5px;
}
.centerd {
    display:table-cell;
}
.component-fade-enter-active, .component-fade-leave-active {
  transition: opacity .3s ease;
}
.component-fade-enter, .component-fade-leave-to
/* .component-fade-leave-active for <2.1.8 */ {
  opacity: 0;
}
</style>
