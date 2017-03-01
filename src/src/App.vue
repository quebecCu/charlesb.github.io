<template>
  <div id="app" class="fullHeight">
    <div class="container-fluid fullHeight">
      <div class="row fullHeight">
        <div id="sideMenu" class="col-md-3 bg-info fullHeight">
          <i class="visible-xs fa fa-2x fa-times menuClose" aria-hidden="true" @click="toggleMenu()"></i>
          <h1 class="text-center">Charles Belzile</h1>
          <p class="text-center">&Eacute;tudiant en informatique originaire du Qu&eacute;bec. Pr&eacute;sentement en France.</p>
          <hr style="color:black;background-color:black;">
          <ul class="nav nav-pills nav-stacked">
            <li v-bind:class="{ active: currentView === 'accueil' }" @click="changeView('accueil')"><a href="#">Accueil</a></li>
            <li v-bind:class="{ active: currentView === 'competences' }" @click="changeView('competences')"><a href="#">Comp&eacute;tences informatique</a></li>
            <li v-bind:class="{ active: currentView === 'experiences' }" @click="changeView('experiences')"><a href="#">Exp&eacute;riences professionelles</a></li>
            <li v-bind:class="{ active: currentView === 'scolaires' }" @click="changeView('scolaires')"><a href="#">Parcours scolaire</a></li>
            <li v-bind:class="{ active: currentView === 'loisirs' }" @click="changeView('loisirs')"><a href="#">Loisirs</a></li>
            <li v-bind:class="{ active: currentView === 'contact' }" @click="changeView('contact')"><a href="#">Contact</a></li>
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
          <i class="visible-xs fa fa-2x fa-bars menuToggle" aria-hidden="true" @click="toggleMenu()"></i>
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
import Contact from './Components/Contact.vue'

export default {
  name: 'app',
  components:{
    accueil: Accueil,
    competences: Competences,
    experiences: Experiences,
    scolaires: Scolaires,
    loisirs: Loisirs,
    contact: Contact
  },
  data () {
    return {
      showLang: false,
      showMenu: false,
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
    },
    changeView(view){
      this.currentView = view
      if (window.innerWidth < 770){
        this.toggleMenu();
      }
    },
    toggleMenu(){
      if (this.showMenu === false){
        var style = document.getElementById('sideMenu').style
        document.getElementById('sideMenu').style.display = 'block';
        this.showMenu = true;
      }else{
        document.getElementById('sideMenu').style.display = 'none';
        this.showMenu = false;
      }
    }
  }
}
</script>

<style>

@media (max-width: 768px) {
  #sideMenu{
    display: none;
    position: fixed;
    z-index: 100;
    top:0px;
    left:0px;
    right:0px;
    left:0px;
    overflow-y: auto;
  }
}

.menuClose{
  position: absolute;
  top: 10px;
  right: 10px;
  opacity: 0.6;
}

.menuToggle{
  position: fixed;
  top: 10px;
  left: 10px;
  opacity: 0.6;
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
