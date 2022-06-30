<template>
    <section class="section-one">
        <h1>Open new tabs is sh*t </h1>
        <div class="section-ctnr">
            <figure class="top-figure"><img  class="desktop-arrows" src="@/assets/left-arrow.svg" alt="">
            <img  class="mobile-arrows top" src="@/assets/mobile-arrow-top.svg" alt=""></figure>
            <div class="middle-ctnr">
                <div>
                    <Frames :text="frame.name" :image="frame.url" />
                </div>
            </div>
            <figure class="bottom-figure"><img  class="desktop-arrows" src="@/assets/right-arrow.svg" alt="">
            <img class="mobile-arrows down" src="@/assets/mobile-arrow-down.svg" alt=""></figure>
        </div>
        <p>
            A solution for your browser tabs and don’t make your device get slower over time. Get ease and faster to
            discover
            a trend with just one tab.</p>
    </section>
</template>

<script>
import Frames from '@/components/SocialFrames.vue'

export default {
    name: 'SectionOne',
    data() {
        return {
            frame: { name: 'Findtrend-Elon Mas', url: require('@/assets/vector.svg') }
        }
    },
    components: {
        Frames,
    }

}
</script>

<style scoped>
.section-one {
    padding: 8.75rem 18.3125rem;
    background: #A8FF35;
    text-align: center;
    color: #000;
}
.mobile-arrows{
    display: none;
}
.section-ctnr {
    margin: 3.75rem auto;
    display: flex;
    justify-content: center;
    align-items: center;

}

.middle-ctnr {
    width: 31.375rem;
    /* height: 12.625rem; */
    padding: 3.75rem 5rem;
    margin: 0 1.625rem;
    background-color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 1rem;

}
h1{
font-weight: 700;
font-size: 72px;
line-height: 86px;
}

p {
    margin: 0 auto;
    width: 666px;
    font-weight: 400;
    font-size: 18px;
    line-height: 150%;
}

@media screen and (max-width: 600px) {
    .section-one{
        padding: 5rem 0.875rem;
    }
    h1{
        font-size: 2.25rem;
    }
    .section-ctnr{
       display: block;
    }
    .middle-ctnr{
        width: 100%;
        padding: 1.5rem;
        margin-left: 0;
    }
    p{
        width: 100%;
    }
    .mobile-arrows{
        display: block;
    }
    .desktop-arrows{
        display: none;
    }
     .top{
        position: relative;
        top:20px;
        left: 260px;
        
    }
    .down{
        position: relative;
        bottom:20px
    }
}
</style>