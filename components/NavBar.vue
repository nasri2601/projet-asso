<template>
    <div>
<header>
<img src="../assets/logo.svg" alt="logo" class="logo">

    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Team</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</header>
<section class="banner"><h1 class="test">"D'un geste! <br> aidé des centaines de diabétiques comme vous."</h1></section>
    </div>
</template>

<script>
    export default {
      
  
    }
</script>

<style>

header{
    background: rgb(0, 0, 0,0.3);
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 10%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: 0.6s;
    padding: 40px 100px;
    z-index: 100000;


}

header .sticky{
    padding: 5px 100px;
    background: white
}

header .logo{

   height: 20vh;
   width: 15%;
   opacity: 0.9;


}

header ul{
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    left: 8%;

}

header ul li{
    position: relative;
    list-style: none;


}
header ul li a:hover{
padding:  30px;
background: rgb(187, 222, 251, 0.4);
    


}
header ul li a{
    
    padding:  30px;
    position: relative;
    margin: 0 15px;
    text-transform: uppercase;
    text-decoration: none;
    color: white;
    letter-spacing: 2px;
    font-weight: bold;
    font-size: 18px;
    transition: 0.5;


}

.banner{
    position: relative;
    width: 100%;
    height: 100vh;
    background: url("../assets/child2.jpg");
    background-size: cover;
    box-shadow: 10px 0px 20px black;
}
.test{
   position: absolute;
   top: 25%;
   left: 25%;
   color: #78909C;
   font-weight: bold;
   font-size: 1.6em;
   transform: translate(-50%, -50%);
}
</style>