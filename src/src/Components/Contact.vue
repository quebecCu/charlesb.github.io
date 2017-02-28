<template>
  <div>
    <h1> Contact </h1>
    <hr style="width:50%;">
    <br>
    <div class="jumbotron">
      <form class="form-vertical" action="https://formspree.io/charles.belzile@hotmail.com" method="POST">
        <div class="form-group">
          <label for="inputEmail" class="col-lg-2 control-label">Email</label>
          <div class="col-lg-10">
            <input type="email" name="email" placeholder="Votre adresse email" class="form-control" id="inputEmail">
          </div>
        </div>
        <br>
        <br>
        <br>
        <br>
        <div class="form-group">
          <label for="textArea" class="col-lg-2 control-label">Message</label>
          <div class="col-lg-10">
            <textarea name="message" placeholder="Votre message" class="form-control" rows="5" id="textArea"></textarea>
          </div>
        </div>
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <div class="form-group">
          <div class="col-lg-10 col-lg-offset-2">
            <button type="submit" class="btn btn-primary">Envoyer</button>
          </div>
        </div>
      </form>
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
