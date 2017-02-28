<template>
  <div>
    <h1> Comp&eacute;tences informatiques </h1>
    <hr style="width:50%;">

    <div class="jumbotron text-left">
      <div class="container text-left">
        <div class="row text-left">
          <div class="col-xs-12 col-sm-3 col-md-2 text-left">
            <span class="fa-stack fa-3x">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i class="fa fa-code fa-stack-1x" style="color:#d9edf7;"></i>
            </span>
          </div>
          <div class="col-xs-12 col-sm-9 col-md-10 text-left">
            <h5>Langages de programmation</h5>
            JAVA, C++, HTML/CSS, Javascript, PHP, Assembleur SPARC, C, XML, SQL
          </div>
        </div>
      </div>
    </div>
    <div class="jumbotron text-left">
      <div class="container text-left">
        <div class="row text-left">
          <div class="col-xs-12 col-sm-3 col-md-2 text-left">
            <span class="fa-stack fa-3x">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i class="fa fa-desktop fa-stack-1x" style="color:#d9edf7;"></i>
            </span>
          </div>
          <div class="col-xs-12 col-sm-9 col-md-10 text-left">
            <h5>Logiciels</h5>
            Eclipse, NetBeans, CodeBlocks, Microsoft Office, IBM Cognos, PostreSQL, SQL Oracle, MySQL
          </div>
        </div>
      </div>
    </div>
    <div class="jumbotron text-left">
      <div class="container text-left">
        <div class="row text-left">
          <div class="col-xs-12 col-sm-3 col-md-2 text-left">
            <span class="fa-stack fa-3x">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i class="fa fa-linux fa-stack-1x" style="color:#d9edf7;"></i>
            </span>
          </div>
          <div class="col-xs-12 col-sm-9 col-md-10 text-left">
            <h5>System d'exploitation</h5>
            Windows, Linux (Ubuntu, RedHat)
          </div>
        </div>
      </div>
    </div>
    <div class="jumbotron text-left">
      <div class="container text-left">
        <div class="row text-left">
          <div class="col-xs-12 col-sm-3 col-md-2 text-left">
            <span class="fa-stack fa-3x">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i class="fa fa-wrench fa-stack-1x" style="color:#d9edf7;"></i>
            </span>
          </div>
          <div class="col-xs-12 col-sm-9 col-md-10 text-left">
            <h5>Outils/Concepts</h5>
            Librairies web (JQuery, Bootstrap, AngularJs, BackboneJs), Design MV*, Git
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'accueil',
  data () {
    return {
      showLang: false
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
