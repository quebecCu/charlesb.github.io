<template>
  <div>
    <h1> Loisirs </h1>
    <hr style="width:50%;">

    <div class="container">
      <div class="row">
        <div class="col-xs-12 col-sm-6 col-md3">
          <img src="../assets/soccer.jpg" class="img-responsive" alt="Soccer">
        </div>
        <div class="col-xs-12 col-sm-6 col-md3">
          <img src="../assets/ski.jpg" class="img-responsive" alt="Soccer">
        </div>
        <div class="col-xs-12 col-sm-6 col-md3">
          <img src="../assets/trekking.jpg" class="img-responsive" alt="Soccer">
        </div>
        <div class="col-xs-12 col-sm-6 col-md3">
          <img src="../assets/velo.jpg" class="img-responsive" alt="Soccer">
        </div>
        <div class="col-xs-12 col-sm-6 col-md3">
          <img src="../assets/informatique.jpg" class="img-responsive" alt="Soccer">
        </div>
        <div class="col-xs-12 col-sm-6 col-md3">
          <img src="../assets/livre.jpg" class="img-responsive" alt="Soccer">
        </div>
        <div class="col-xs-12 col-sm-6 col-md3">
          <img src="../assets/bierre.jpg" class="img-responsive" alt="Soccer">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
var Waterfall = require('vue-waterfall')

export default {
  name: 'accueil',
  components: {
    'waterfall': Waterfall.waterfall,
    'waterfall-slot': Waterfall.waterfallSlot,
  },
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
