<template>
    <div id="container">
        <Header/>
        <div class="main">
            <router-view/>
        </div>
        <Footer/>
    </div>
</template>

<script>
import Header from "@/components/Header.vue"
import Footer from "@/components/Footer.vue"

export default {
    name: 'Homeindex',
    components: {
        Header,
        Footer
    }
}
</script>

<style scoped>
    #container{
        width:1080px;
        height:100%;
        margin:auto;
        padding-top:20px;
        
    }
    .main{
        min-height: calc(100vh - 380px);
        padding-top:50px;
    }

    @media (max-width: 1280px) {
        #container{
            width:80%;
        }
    }
    @media (max-width: 700px) {
        #container{
            width:90%;
        }
    }
</style>