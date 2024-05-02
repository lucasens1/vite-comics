<script>
export default {
    data(){
        return {
            //Lista icone
            icons_list : [
                {
                    icon : "digital-comics.png",
                    desc : "DIGITAL COMICS"
                },
                {
                    icon : "merchandise.png",
                    desc : "DC MERCHANDISE"
                },
                {
                    icon : "subscriptions.png",
                    desc : "SUBSCRIPTION"
                },
                {
                    icon : "shop-locator.png",
                    desc : "COMIC SHOP LOCATOR"
                },
                {
                    icon : "power-visa.svg",
                    desc : "DC POWER VISA"
                },
            ],
        };
    },
    methods : {
        getImagePath(iconName){ 
            return new URL(`../assets/img/buy-comics-${iconName}`, import.meta.url).href;
        },
    }
};
</script>

<template>
    <div class = "wrapper primary-blue">
        <div class = "w-80 pd-20">
            <ul>
                <li v-for = "item in icons_list">
                    <img :src="getImagePath(item.icon)"/>
                    <span>  {{item.desc}} </span>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/_mixins" as *;
@use "../style/partials/_variables" as *;
@import '../style/generals.scss';

ul {
    @include flex(row, space-evenly, center);
    list-style-type : none;
    gap : 10px;
    padding : 10px;
    li{
        @include flex(row, center, center);
        gap : 8px;
        img {
            height : 60px;
        }
        span {
            color : white;
        }
    }
}

</style>