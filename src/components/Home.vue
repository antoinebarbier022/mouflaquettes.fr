<template>
    <div class="home">
        <div class="link-streaming">  
            <ButtonMusic    class="button-music" title="Youtube"        
                            img="yt_logo_rgb_dark.png"                  
                            link="www.youtube.com/channel/UCIyHFPn31xBb44gqxkoVn9g"
                            data-aos="fade-right"
                            data-aos-duration="1500"
            />
            <ButtonMusic    class="button-music" 
                            title="Deezer"         
                            img="Colored_Full_White@2x.png"             
                            link="www.deezer.com/fr/artist/54676462"
                            data-aos="fade-left"
                            data-aos-duration="1500"
            />
            <ButtonMusic    class="button-music" 
                            title="Spotify"        
                            img="Spotify_Logo_RGB_Green.png"            
                            link="open.spotify.com/artist/09pFOn63ilNCmgccHtQyqE"
                            data-aos="fade-right"
                            data-aos-duration="2500"
            />
            <ButtonMusic    class="button-music" 
                            title="Apple Music"    
                            img="US-UK_Apple_Music_lockup_RGB_wht.svg"  
                            link="itunes.apple.com/ca/artist/mouflaquettes/1444479500"
                            data-aos="fade-left"
                            data-aos-duration="2500"
            />
        </div>
        
        <router-link :to="{name: 'notre-groupe'}">
            <figure class="img-mouflaquettes">
                <img src="@/assets//photos/mouflaquettes.png" alt="">
                <legend><router-link :to="{name: 'notre-groupe'}" title="Notre groupe" class="text-notre-groupe">Découvrir notre Groupe !</router-link></legend>
            </figure>
            <!--<div class="img-mouflaquettes">
            </div>-->
        </router-link>
        
    </div>
</template>

<script>
import ButtonMusic from "@/components/buttons/button-music.vue"

export default {
    name: "Home",
    components:{
        ButtonMusic
    }
}
</script>

<style scoped>
    .home{
        width:100%;
        height:100%;
        display:flex;
            flex-direction: column;
        /* placer le footer en bas de la page notre groupe */
            min-height: calc(100vh - 380px); /* - hauteur du footer et - hauteur du header - 
                                                                    20px(hauteur du padding-top du container) - hauteur du padding-top de ce bloc*/

    }
    .link-streaming{
        width:100%;
        display:flex;
            flex-direction: row;
            flex-wrap: wrap;
            justify-content:center;
        padding-bottom:50px;
    }
    .button-music{
        margin:20px;
        margin-bottom:0;
    }

    .img-mouflaquettes img{
        width:80vw;
        max-width:80%;
        /*height:50vh;
        background-image: url('~@/assets/mouflaquettes.png');
        background-repeat: no-repeat;
        background-size:contain;
        background-position:center;*/

    }


    legend .text-notre-groupe{
        display:none;
        width:100%;
        text-align: center;

        padding-top:5px;
        padding-bottom:5px;
        margin-bottom:20px;
        cursor:pointer;
        font-weight: 700;
        font-size: 18px;
        border:1px solid rgba(255, 255, 255, 0.705);
        border-radius: 5px;
        background-color:rgba(255, 255, 255, 0.15);
        
    }
    

     @media (max-width: 1080px) {
         .home{
             flex-direction: column;
         }
         .img-mouflaquettes{
             width:100%;
             padding-bottom:0px;
             background-size:contain 80%;
              background-position:top;
         }
         .link-streaming{
             width:100%;
             height:280px;
             flex-direction:column;
             justify-content:flex-start;
         }
        .button-music{
            margin: auto;
            margin-bottom:0;
            margin-top:20px;
        }
     }

         @media (max-width: 550px) {
            legend .text-notre-groupe{
                display:flex;
                    justify-content: center;
                    align-content: center;
            }
            figure{
                display:flex;
                flex-direction: column;
                justify-content: center;
                    align-items: center;
            }
            legend{
                display:block;
                width:80%;
                justify-items: center;
            }
        }
     

</style>