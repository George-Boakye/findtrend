<template>
    <header>
        <Navbar />
        <h1 class="first-heading">Minimize your tabs.</h1>
        <h1>Find the trends!</h1>
        <p class="header-paragraph">Don't let your computer memorles consumes all of those browser tabs.
            Findtrend let you gathers all of your favorite website into one place.</p>
        <div class="hero-btn-ctnr">
            <Button class="green-button" text="Get started 🔥" :style="{ 'background-color': '#A8FF35' }" />
            <figure><img src="@/assets/img-hero.svg" alt=""></figure>
        </div>
        <div class="frame-container">
            <Frames v-for="social in socials" :key="social.id" :text="social.name" :image="social.url"
                :name="social.id" />
        </div>
    </header>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Button from '@/components/Button.vue'
import Frames from '@/components/SocialFrames.vue'
export default {
    name: 'Header',
    components: {
        Navbar, Button, Frames,
    },
    data() {
        return {
            socials: [{ id: 'twitter', name: 'Cryptopunk-Search', url: require('@/assets/twitter-logo.svg') },
            { id: 'pinterest', name: 'Popular Design-Se', url: require('@/assets/pinterest-logo.svg') },
            { id: 'facebook', name: 'Product Design-Se', url: require('@/assets/facebook-logo.svg') },
            { id: 'dribble', name: 'Elon Musk-Search', url: require('@/assets/dribble-logo.svg') },
            ],

        }
    },
}
</script>

<style>
header {
    background-image: url('@/assets/background-img.svg');
    background-size: cover;
    color: #fff;
    text-align: center;
}

h1 {
    font-weight: 900;
    font-size: 4.5rem;
    line-height: 112%;
}

.first-heading {
    margin-top: 8.75rem;
}

.header-paragraph {
    margin: 1.5rem auto;
    margin-bottom: 2.5rem;
    width: 39.125rem;
    height: 3.375rem;
    font-weight: 400;
    font-size: 1.125rem;
    line-height: 150%;
    color: #8B8B8B;
}

.hero-btn-ctnr {
    display: flex;
    justify-content: center;
    align-items: center;
}

Button {
    font-weight: 700;
    font-size: 1.125rem;
    line-height: 140%;
    text-align: center;
    color: #000;
    border: none;
}

.green-button {
    width: 195px;
    height: 3.5625rem;
    padding: 1rem 2rem;
    margin-right: 1.125rem;
}

.frame-container {
    margin-top: 96px;
    position: relative;
    height: 200px;
}


@media screen and (max-width: 600px) {
header{
padding: 0 1.75rem;
padding-bottom: 3.125rem;
}
h1 {
    font-size: 2.25rem;
}
.first-heading {
margin-top: 5rem;
}
.header-paragraph{
    font-size: 0.875rem;
    width: 100%;
}
.hero-btn-ctnr figure{
    display: none;
}
.frame-container{
    height: max-content;
}

}
</style>