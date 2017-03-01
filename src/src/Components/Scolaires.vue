<template>
  <div>
    <h1> Parcours scolaire </h1>
    <hr style="width:50%;">
    <div class="jumbotron text-left">
      <div class="container text-left">
        <div class="row text-left">
          <div class="col-xs-12 col-sm-3 col-md-2 text-left">
            <img src="../assets/insa.png" class="img-responsive" alt="Insa Lyon">
          </div>
          <div class="col-xs-12 col-sm-9 col-md-10 text-left">
            <h5><a href="https://www.insa-lyon.fr/">INSA Lyon</a></h5>
            <h6> &Eacute;change &eacute;tudiant. D&eacute;partement d'informatique - Janvier 2017 &agrave; Mai 2017</h6>
          </div>
        </div>
      </div>
    </div>
    <div class="jumbotron text-left">
      <div class="container text-left">
        <div class="row text-left">
          <div class="col-xs-12 col-sm-3 col-md-2 text-left">
            <img src="../assets/sherbrooke.png" class="img-responsive" alt="Universite de Sherbrooke">
          </div>
          <div class="col-xs-12 col-sm-9 col-md-10 text-left">
            <h5><a href="https://www.usherbrooke.ca/">Universit&eacute; de Sherbrooke</a></h5>
            <h6> Informatique de gestion - 2014 &agrave; 2017</h6>
          </div>
        </div>
      </div>
    </div>
    <div class="jumbotron text-left">
      <div class="container text-left">
        <div class="row text-left">
          <div class="col-xs-12 col-sm-3 col-md-2 text-left">
            <img src="../assets/maisonneuve.png" class="img-responsive" alt="Maisonneuve">
          </div>
          <div class="col-xs-12 col-sm-9 col-md-10 text-left">
            <h5><a href="http://www.cmaisonneuve.qc.ca/">Coll&egrave;ge de Maisonneuve</a></h5>
            <h6> DEC en Sciences Informatiques et Math&eacute;matiques - 2014</h6>
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
      showLang: false,
      currentView: 'accueil'
    }
  },
  methods:{

  }
}
</script>
