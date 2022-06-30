<template>
    <nav>
        <figure class="logo">
            <img class="desktop-logo" src='../assets/logocolor.svg' alt="">
            <img  class="mobile-logo" src='../assets/mobile-vector.svg' alt="">
        </figure>
        <figure class="menu" @click="displayMenu()">
            <img class="hamburger"  src="@/assets/harmburger.svg" alt="">
            <img  class="close" src="@/assets/close-icon.svg" alt="">
        </figure>
        <div class="links m-links" :class="[toggle === true? m-links: '']">
            <div>
                 <a href="">About</a>
            <a href="">How it works</a>
            <a href="">Pricing</a>
            <a href="">Solution</a>
            <a href="">Features</a>
             <a class="right-nav" href="">Login</a>
            <Button text='Register'/>
            </div>
        </div>
       
    </nav>
</template>

<script>
import Button from '@/components/Button.vue'

export default {
    name: 'Navbar',
    components:{Button},
    data(){
         
        return{
            toggle:false,
    
        }
    
    },
    methods:{
        displayMenu(){
                  this.toggle = !this.toggle
            console.log(this.toggle)
            }
          
        },

    computed:{
        display(){
            
               return this.toggle

        }
    }
    }
</script>

<style scoped>
nav {
    padding: 1.8125rem 5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-weight: 400;
    font-size: 1.125rem;
    line-height: 100%;
    position: relative;
}

a {
    text-decoration: none;
    color: #fff;
    margin-right: 2.5rem;
}
.right-nav{
    margin-left: 11.4375rem;
}
Button{
     font-weight: 400;
    font-size: 1.125rem;
    line-height: 100%;
}
.menu{
    display:none
}
.mobile-logo{
    display: none;
}


@media screen and (max-width: 600px){
nav{
    display: block;
    /* flex-direction: column;
    justify-content:center; */
    padding: 1.5rem 1.125rem;
    width: 100%;
    background: #000;
}
a{
    display: block;
    margin-bottom: 40px;
    margin-right: 0;
}
.right-nav{
    margin-left: 0;
}
.menu{
    display: block;
    position: absolute;
    right: 0;
}
.close{
    display: none;
}
.m-links{
    height: 552px;
    width: 100%;
    left: 0;
    position: absolute;
    margin-top:104px;
    background-color: #000;
    z-index: 3;
    /* display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center; */
}
.logo{
position: absolute;
left: 0;
}
.logo img{
    width: 100%;
}
.desktop-logo{
    display: none;
}
.mobile-logo{
    display: block;
}
}
</style>