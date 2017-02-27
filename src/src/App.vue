<template>
  <div id="app" class="fullHeight">
    <div class="container-fluid fullHeight">
      <div class="row fullHeight">
        <div class="col-xs-12 col-md-3 bg-info fullHeight">
          <h1 class="text-center">Charles Belzile</h1>
          <p class="text-center">&Eacute;tudiant en informatique originaire du Qu&eacute;bec. Pr&eacute;sentement en France.</p>
          <hr style="color:black;background-color:black;">
          <ul class="nav nav-pills nav-stacked">
            <li class="active"><a href="#">Accueil</a></li>
            <li><a href="#">Comp&eacute;tences informatique</a></li>
            <li><a href="#">Exp&eacute;rience proffessionel</a></li>
            <li><a href="#">Parcours scolaire</a></li>
            <li><a href="#">Loisirs</a></li>
            <li><a href="#">Contact</a></li>
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
        <div class="col-xs-12 col-md-9 text-center">
          <img src="./assets/page-en-construction.png" style="margin-top:20px;"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: {
    showLang: false
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
</style>
