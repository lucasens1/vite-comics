<script>
//Importo Array e Card
import { arrayDC } from "../assets/data/comicsArray.js"; 
import AppCard from "./AppCard.vue"; 

export default {
  components: {
    AppCard,
  },
  data() {
    return {
      //Assegno l'array a comics
      comics : arrayDC,
    };
  },
};
</script>

<template>
    <div class="bg-black jumbotron">
        <div>
            <img src="../assets/img/jumbotron.jpg" alt="">
        </div>
    </div>
    <section class="comics-section">
        <div class="row">
          <div class="col" v-for="comic in comics">
              <AppCard
                :img ="comic.thumb"
                :name ="comic.series"
                :altext ="comic.type"
              />
          </div>
        </div>
      </section>
</template>

<style lang = "scss" scoped>
/* Importo flex */
@use "../style/partials/_mixins" as *;
/* Importo le classi dal file generals.scss */
@import '../style/generals.scss';



.bg-black {
    background-color : black;
    width : 100%;
    color : white;
}

.jumbotron{
    height: 450px;
    img{
        max-height: 450px;
        width: 100%;
        object-fit: fill;
    }
}


.comics-section {
  margin-top: 2rem;
  padding: 3rem 3rem;

  @include flex(column, center, center);

  .row {
    @include flex(row, space-between, stretch);
    flex-wrap: wrap;
    .col {
      width: calc(100% / 6);
      margin-bottom: 1.5rem;
    }
  }
}
</style>