<script>
export default {
    data(){
        return {
            //Array di oggetti contenenti titolo della voce nell'header e indicatore Flag della classe active
            menu_items : [
                {
                    title : "Characters",
                    activeFlag : false
                },
                {
                    title : "Comics",
                    activeFlag : true
                },
                {
                    title : "Movies",
                    activeFlag : false
                },
                {
                    title : "TV",
                    activeFlag : false
                },
                {
                    title : "Games",
                    activeFlag : false
                },
                {
                    title : "Collectibles",
                    activeFlag : false
                },
                {
                    title : "Videos",
                    activeFlag : false
                },
                {
                    title : "Fans",
                    activeFlag : false
                },
                {
                    title : "News",
                    activeFlag : false
                },
                {
                    title : "Shop",
                    activeFlag : false
                },
            ],
        };
    },
};
</script>

<template>
    <header>
      <div class="header-logo">
        <img
          src="../assets/img/dc-logo.png"
          alt="Logo DC"
        />
      </div>
      <ul>
        <li v-for = "item in menu_items" :class="{ active : item.activeFlag }">
            <a href = "#" :class="{ active : item.activeFlag }">{{item.title}}</a></li>
      </ul>
    </header>
  </template>

<style lang="scss" scoped>
@use "../style/partials/_mixins" as *;
@use "../style/partials/_variables" as *;

header {
    @include flex(row, space-between, center);
    background-color : $header_color;
    width : 80%;
    margin : 0 auto;
    padding : 10px;
    margin-top : 10px;
        ul{
            display : flex;
            gap : 1rem;
            li{
               list-style-type : none;
               padding : 8px 8px;

               &.active {
                border-bottom : 2px solid $primary_blue;
               }

               a{
                text-decoration : none;
                color : black;
                display : inline-block;

                &.active {
                    color : $primary_blue;
                }
               }
            }
        }
}

</style>