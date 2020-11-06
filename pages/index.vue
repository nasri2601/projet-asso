<template>
  <div>
    <NavBar class="nav"/>
    
    
      <div class="blank2" />
       <v-container>
        <div class="wrapper2">
          <v-container><img src="../assets/images.jpg" alt="logo" class="img0"></v-container>
          <div class="firstTitle"><h1 >Qui sommes nous</h1></div><div class="firstParagraph"><h2>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sunt porro molestiae id dignissimos nisi ex rerum ullam? Sed exercitationem repellendus quisquam, explicabo tempore quos ipsum animi optio earum odio excepturi.</h2>
          <v-btn  color="#1E88E5" class="btn1" outlined large><p class="textBtn">A propos de nous</p> </v-btn>
          </div>
        </div>
<div class="blank2" />
        </v-container>
<div class="blank" />
    <div class="wrapper">
      <div class="img1"/>
      <h2 class="title1">lorem ipsum <br><span>blablaba</span></h2>
      <div class="img2"/>
      <h2 class="title2">lorem ipsum <br>test <br><v-btn outlined color="#1E88E5" class="btn" large><p class="textBtn">Comment aider</p></v-btn></h2>
      
    </div>
    
    
    <div class="blank" />
    <div class="wrapper3">

<v-container>
        <div class="articlesTitle">
          <h1>Actualité</h1>
        </div>
        <div class="articlesparagraph"><h2>Loremde ipsum dolor sit amet consectetur adipisicing elit. Iusto, sequi perferendis.</h2></div>
        <Articles class="articles"/>
        <v-btn  color="#1E88E5" class="btn2" outlined large><p class="textBtn">Toutes les actualités...</p> </v-btn>
        
        <div class="wrapper4"><div class="donTitle" ><h2>Vos derniers dons</h2></div>
        <div class="donParagraph"><h2>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto, sequi perferendis.</h2></div><Caroussel class="caroussel"/></div>
        
        
        <Footer/>
      </v-container>

    </div>

  </div>
</template>

<script>
import { gsap } from 'gsap'
import NavBar from '@/components/NavBar.vue';
import Articles from '@/components/Articles.vue';
import Footer from '@/components/Footer.vue';
import Caroussel from '@/components/Caroussel.vue';
export default {
  components: {
    NavBar,
    Articles,
    Footer,
    Caroussel
  },
  mounted () {
    this.startAnimations()
    this.startTitleAnimation()
    this.startArticlesAnimation()
    this.startDonAnimation()
  },
  methods: {
    startAnimations () {
  let tl = new TimelineMax({onUpdate:updatePercentage})
  
  tl.to(".img1", 1, {width:"100%" , height:"100%"}, 0)
  tl.to(".title1", 0.5, {opacity: 1},1)
  tl.to(".title1", 0.5, {opacity: 0},2)
  tl.to(".img2", 1, {height:"100%"}, 1.5)
  tl.from(".title2",1 ,{opacity: 0},2.2)
  tl.to(".img1", 0 ,{opacity: 0},3)
  tl.to(".img2", 1,{width: "60%", height: "60%", transform: "translate(20%, 0%)"}, 3)
  tl.to(".nav", 1,{opacity:0}, 2)
  tl.from(".nav",1 ,{opacity: 1},3)
  tl.to(".title2",0.1 ,{color: "rgba(0, 0, 0, 0)"}, 3)
  tl.to(".btn",0 ,{opacity:0 }, 3)
  



  const scene = this.$scrollmagic.scene({
    triggerElement: '.wrapper',
    triggerHook: 0,
    duration: "300%"
  })
  .setPin(".wrapper")
  .setTween(tl)
  this.$scrollmagic.addScene(scene)

  function updatePercentage(){
    tl.progress()
  }
    },

    startTitleAnimation(){
      let tl = new TimelineMax({onUpdate:updatePercentage})
tl.to(".img0",1 ,{opacity: 1},1)
tl.to(".firstTitle",1 ,{opacity: 1},1.5)
tl.to(".firstParagraph",1 ,{opacity: 1},1.7)
tl.to(".btn1",1 ,{opacity: 1},2.2)
       const scene = this.$scrollmagic.scene({
    triggerElement: '.wrapper2',
    triggerHook: 0,
    duration: "150%"
  })
  .setPin(".wrapper2")
  .setTween(tl)
  this.$scrollmagic.addScene(scene)

  function updatePercentage(){
    tl.progress()
  }
    },
       startArticlesAnimation(){
      let tl = new TimelineMax({onUpdate:updatePercentage})
tl.to(".articlesTitle",6 ,{opacity: 1},1)
tl.to(".articlesparagraph",1 ,{opacity: 1},2)
tl.to(".articles",6 ,{opacity: 1},3)

const scene = this.$scrollmagic.scene({
    triggerElement: '.wrapper3',
    triggerHook: 0,
    duration: "150%"
  })
  .setPin(".wrapper3")
  .setTween(tl)
  this.$scrollmagic.addScene(scene)

  function updatePercentage(){
    tl.progress()
  }
    },
           startDonAnimation(){
      let tl = new TimelineMax({onUpdate:updatePercentage})

tl.to(".donTitle",1 ,{opacity: 1},1)
tl.to(".donParagraph",6 ,{opacity: 1},2)
tl.to(".caroussel",6 ,{opacity: 1},2.2)

const scene = this.$scrollmagic.scene({
    triggerElement: '.wrapper4',
    triggerHook: 0,
    duration: "150%"
  })
  .setPin(".wrapper4")
  .setTween(tl)
  this.$scrollmagic.addScene(scene)

  function updatePercentage(){
    tl.progress()
  }
    }
  }
}
</script>
<style>
.nav{
  opacity: 1;
}
 html{
   box-sizing: border-box;
   font-size: 100%;
 }

 *, *:before, *:after{
   box-sizing: inherit;
   margin: 0;
   padding: 0;
 }

 body{
   width: 100%;
   -webkit-font-smoothing: antialiased;
   font-family: 'open sans' ,sans-serif;
   overflow-x: hidden;
   color: black;
   font-size: 16px;

 }

 .blank{
   width: 100%;
   height:1vh;

 }
 .blank2{
    width: 100%;
   height:1vh;
 }

 .wrapper{
   width: 100%;
   height: 100vh;
   position: relative;
   display: flex;
   justify-content: center;
   align-items: flex-end;
   overflow: hidden;
 }
 
 
 .img0{
   width: 30%;
 margin-left: 35%;
 margin-top: 5%;
 opacity: 0;
   
 }
 .btn1{
   margin-top: 2%;
   opacity: 0;
 }
 .btn2{
   margin-left: 40%;
   margin-bottom: 20%;
 }
 .textBtn{
   font-weight: bold;
 }

 .img1{
   background-image: url('../assets/child.jpg');
   width: 60%;
   height: 60%;
   background-size: cover;
   background-repeat: no-repeat;
   background-position: center center;
 }
  .firstTitle{
    font-size: 40px;
   transform-origin: center center;
   text-align: center;
   margin-top:  0;
   opacity: 0;
  }
 

  .firstParagraph{
    color: #78909C;
    transform-origin: center center;
   text-align: center;
   margin-top:  5%;
   opacity: 0;
  }
  .articlesTitle{
     font-size: 40px;
   transform-origin: center center;
   text-align: center;
   margin-top:  15%;
   opacity: 0;
  }

  .donTitle{
   font-size: 40px;
   transform-origin: center center;
   text-align: center;
   margin-top:  10%;
   opacity: 0;
  }
  .donParagraph{
    color: #78909C;
    transform-origin: center center;
    text-align: center;
    opacity: 0;
    margin-bottom: 3%;

  }
  .caroussel{
    opacity: 0;
    margin-bottom: 5%;
    box-shadow: 10px 0px 30px black;
  }
  .articlesparagraph{
    color: #78909C;
    transform-origin: center center;
   text-align: center;

   opacity: 0;
  }
  .articles{
    opacity: 0;
  }
 .title1{
   position: absolute;
   top: 45%;
   left: 11%;
   font-size: 40px;
   transform: translate(-50%, -50%);
   opacity: 0;
 }

 .title1 span{
   font-size: 24px;
   font-weight: 400;
   display: block;
 }

 .img2{
   background-image: url('../assets/happy.jpg');
   width: 100%;
   height: 0;
   position: absolute;
   bottom: 0;
   left: 0%;
   transform: translate(-50% 0);
   background-size: cover;
   background-repeat: no-repeat;
   background-position: center bottom;
 }

 .title2{
   position: absolute;
   top: 50%;
   left: 15%;
   font-size: 60px;
   transform: translate(-50%,-50%);
   transform-origin: center center;
   text-align: center;
   line-height: 60px;

 }


</style>
