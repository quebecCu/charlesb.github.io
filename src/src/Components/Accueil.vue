<template>
  <div>
    <h2> &Eacute;tudiant en informatique de gestion </h2>
    <hr style="width:50%;">
    <h4>
      Je suis une personne curieuse, toujours pr&ecirc;t &agrave; en apprendre d'avantage sur toute sorte de sujet.
    </h4>
    <h5>
      J'ai d'abord d&eacute;couvert la programmation avec le langage JAVA &agrave; l'&eacute;cole dans un cours &agrave; option. <br>
      C'est cette d&eacute;couverte qui m'a donn&eacute; l'envie d'aller plus loin dans le domaine de l'informatique.
    </h5>
    <br>
    <br>
    <div class="jumbotron text-left">
      <div class="container text-left">
        <div class="row text-left">
          <div class="col-xs-2 text-left">
            <span class="fa-stack fa-3x">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i class="fa fa-file-text fa-stack-1x" style="color:#d9edf7;"></i>
            </span>
          </div>
          <div class="col-xs-10 text-left">
            <h5>Gestion de l'informatique</h5>
            &Eacute;tudiant l'informatique de gestion, j'&eacute;prouve un grand int&eacute;r&egrave;t &agrave; &eacute;tudier comment les technologies de l'information influence le milieu
            dans lequel il se trouve. Que ce soit dans une organisation ou pour un individuel, j'aime trouver des solutions informatiques pour faciliter certains aspects de nos vie.
          </div>
        </div>
      </div>
    </div>
    <div class="jumbotron text-left">
      <div class="container text-left">
        <div class="row text-left">
          <div class="col-xs-2 text-left">
            <span class="fa-stack fa-3x">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i class="fa fa-code fa-stack-1x" style="color:#d9edf7;"></i>
            </span>
          </div>
          <div class="col-xs-10 text-left">
            <h5>Web</h5>
            Les nouvelles technologies web m'int&eacute;resse beaucoup. J'ai d'abord commenc&eacute; avec HTML et CSS.
            J'ai ensuite d&eacute;couvert Javascript ainsi que les diff&eacute;rents <i>Framework</i> disponibles. Ce qui m'a d'ailleurs amen&eacute; &agrave; cr&eacute;er ce site.
          </div>
        </div>
      </div>
    </div>
    <div class="jumbotron text-left">
      <div class="container text-left">
        <div class="row text-left">
          <div class="col-xs-2 text-left">
            <span class="fa-stack fa-3x">
              <i class="fa fa-circle fa-stack-2x"></i>
              <i class="fa fa-btc fa-stack-1x" style="color:#d9edf7;"></i>
            </span>
          </div>
          <div class="col-xs-10 text-left">
            <h5>Technologie Blockchain</h5>
            Lorsque j'ai entendu parler pour la premi&egrave;re fois du Bitcoin, j'ai tout de suite &eacute;t&eacute; int&eacute;resse&eacute; par cette technologie.
            J'essaie de m'informer le plus possible sur ce sujet ainsi que sur la technologie qui se trouve &agrave; l'arri&egrave;re de ce concept: la Blockchain.
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
