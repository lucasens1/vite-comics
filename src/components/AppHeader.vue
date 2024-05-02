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
        <li v-for = "item in menu_items">{{item.title}}</li>
      </ul>
    </header>
  </template>

<style lang="scss" scoped>
</style>