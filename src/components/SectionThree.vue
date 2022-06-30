<template>
  <section>
    <h2>All platform connect to Findtrend</h2>
    <div class="socials-container">
        <div class="socials" :class="social.id" v-for="social in socials" :key="social.id">
            <figure>
                <img :src="social.url" alt="">
            </figure>
        </div>
    </div>
    <div class="tweets-container">
        <div class="tweet" v-for="tweet in tweets" :key="tweet.id">
        <figure>
            <img :src="tweet.url" alt="">
        </figure>
        </div>
    </div>
    <Button text="View More Trend" />
  </section>
</template>

<script>

 import Button from '@/components/Button.vue'

export default {
name:'SectionThree',
data(){
    return{
        socials:[
            {id:'facebook', url:require('@/assets/facebook.svg')},
            {id:'twitter', url:require('@/assets/twitter.svg')},
            {id:'dribble', url:require('@/assets/dribble.svg')},
            {id:'pinterest', url:require('@/assets/pinterest.svg')},
            {id:'medium', url:require('@/assets/medium.svg')},
            {id:'reddit', url:require('@/assets/reddit.svg')},
            {id:'vk', url:require('@/assets/vk.svg')},
            {id:'linkedin', url:require('@/assets/linkedin.svg')},],
        tweets:[
                 {id:'tweet1', url:require('@/assets/tweet1.svg')},
                 {id:'tweet2', url:require('@/assets/tweet2.svg')},
                 {id:'tweet3', url:require('@/assets/tweet3.svg')},
        ],
        
    }
},
components:{Button}
}
</script>

<style scoped>
section{
    padding: 8.75rem;
    text-align: center;
    background: #FAFAFA;
}
h2{
font-weight: 700;
font-size: 4rem;
line-height: 4.75rem;
}
.socials-container{
    margin: 5rem 0;
    display: flex;
    justify-content: space-between;
    overflow-x: hidden;

}
.socials{
    background: #fff;
    width: 7.75rem;
/* height: 7.75rem; */
display: flex;
justify-content: center;
align-items: center;
border-radius: 0.5rem;
}
.socials figure{
    padding: 2rem;
}
.twitter{
    background-color: #A8FF35;;
}
.tweet{
    margin-bottom:2.6875rem;
}
Button{
    height:57px;
     width: 198px;
     color: #fff;
     background-color: #000;
}

@media screen and (max-width: 600px) {
    section{
        padding: 5rem 1.125rem;
    }
    h2{ 
        font-size: 2.25rem;
        font-weight: 900;
        line-height: 2.6875rem;
    }
    .socials{
        margin-right: 0.9375rem;
    
    }
    .socials figure{
        padding: 1rem;
        width: 100%;
    }
    .socials img{
        width: 2.5rem;
        height: 2.5rem;
    }
    .tweet{
        width: 100%;
        margin-bottom: 1rem;
    }
    .tweet img{
        width: 100%;
    }
}
</style>