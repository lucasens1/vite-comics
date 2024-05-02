<script>
export default {
    data(){
        return {
            foot_list : [
                {
                    title : "DC COMICS",
                    sub_list : [
                        {
                            vox : "Characters"
                        },
                        {
                            vox : "Comics"
                        },
                        {
                            vox : "Movies"
                        },
                        {
                            vox : "TV"
                        },
                        {
                            vox : "Games"
                        },
                        {
                            vox : "Videos"
                        },
                        {
                            vox : "News"
                        },
                    ],
                },
                {
                    title : "SHOP",
                    sub_list : [
                        {
                            vox : "Shop DC"
                        },
                        {
                            vox : "Shop DC Collectibles"
                        },
                    ],
                },
                {
                    title : "DC",
                    sub_list : [
                        {
                            vox : "Terms Of Use"
                        },
                        {
                            vox : "Privacy Policy (New)"
                        },
                        {
                            vox : "Ad Choices"
                        },
                        {
                            vox : "Advertising"
                        },
                        {
                            vox : "Jobs"
                        },
                        {
                            vox : "Subscriptions"
                        },
                        {
                            vox : "Talent Workshops"
                        },
                        {
                            vox : "CPSC Certificates"
                        },
                        {
                            vox : "Ratings"
                        },
                        {
                            vox : "Shop Help"
                        },
                        {
                            vox : "Contact Us"
                        }
                    ],
                },
                {
                    title : "SITES",
                    sub_list : [
                        {
                            vox : "DC"
                        },
                        {
                            vox : "MAD Magazine"
                        },
                        {
                            vox : "DC Kids"
                        },
                        {
                            vox : "DC Universe"
                        },
                        {
                            vox : "DC Power Visa"
                        }
                    ],
                },
            ],
        };
    },
};
</script>

<template>
    <footer class="wrapper">
        <div class = "w-80">
            <ul v-for="titleList in foot_list">
                <h4>{{ titleList.title }}</h4>
                <li v-for="subL in titleList.sub_list">
                    {{ subL.vox }}
                </li>
            </ul>
            <div class = "bg">
            </div>
        </div>
        
    </footer>
</template>

<style lang="scss" scoped>
@use "../style/partials/_mixins" as *;
@use "../style/partials/_variables" as *;
@import '../style/generals.scss';

footer{
    background-image : url('../assets/img/footer-bg.jpg');
    background-repeat : no-repeat;
    background-size : cover;
    /* Flexo il footer impostando il div in colonna*/
    display : flex;
    flex-direction : column;
    div{
        display : flex;
        flex-wrap : wrap;
        flex-direction : column;
        align-items : flex-start;
        /* Imposto un altezza massima */
        max-height : 300px;
        gap : 10px;

        ul{
            padding : 20px;
            width : 15%;
            h4{
                color : white;
                font-size : 1.4rem;
            }
            li{
                color : lightgrey;
                font-size : 0.8rem;
                list-style-type : none;
            }
        }
        div{
            width :80%;
            height : 300px;
            background-image : url('../assets/img/dc-logo-bg.png');
            background-size : contain;
            background-repeat : no-repeat;
            background-position : center;
        }  
    }
}

</style>