<template>
    <nav>
        <figure class="logo">
            <img class="desktop-logo" src='../assets/logocolor.svg' alt="">
            <img  class="mobile-logo" src='../assets/mobile-vector.svg' alt="">
        </figure>
        <figure class="menu" @click="displayMenu()">
            <img class="hamburger" :class="[toggle? hamburger: '']" src="@/assets/harmburger.svg" alt="">
            <img  class="close" :class="[toggle? close: '']" src="@/assets/close-icon.svg" alt="">
        </figure>
        <div class="links" :class="[toggle? menu: '', link]">
            <div class="container">
                 <a href="">About</a>
            <a href="">How it works</a>
            <a href="">Pricing</a>
            <a href="">Solution</a>
            <a href="">Features</a>
             <a class="right-nav" href="">Login</a>
            <Button text='Register'/>
            </div>
            <div class="overlay"></div>
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
            menu:"m-links",
            link: 'links',
            hamburger:'hambg',
            close:'close2'



        }
    },
    methods:{
        displayMenu(){
                  this.toggle = !this.toggle
            console.log(this.toggle)
            }
        },
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
    z-index: 5;
}
.hambg{
    display: none;
}
.close{
    display: none;
}
.close2{
display: block;
}
.links{
    display:none;
}
.container{
    z-index: 10;
    position: absolute;
    width:100%;
}
.overlay{
    background-color: #000;
    position: fixed;
    left:0;
    bottom:0;
    width: 100%;
    opacity: 0.5;
    height:100%;
}
.m-links{
    height: 552px;
    width: 100%;
    left: 0;
    position: absolute;
    margin-top:104px;
    background-color: #000;
    z-index: 3;
    display: block;
    /* display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center; */
}
.logo{
position: absolute;
left: 0;
z-index: 5;
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