<template>
    <div class="frame" :class="name">
        <div class="info">
            <figure><img :src="image" alt=""></figure>
            <div class="p-text">
                     <p>{{ text }}</p>
            </div>
            <div class="cross">
                <figure>
                    <img src="@/assets/cross.svg" alt="">
                </figure>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'SocialFrames',
    props: ['text', 'image', 'name']
}
</script>

<style scoped>


.frame {
    background: #000;
    width: 341.23px;
    padding: 23px 21px;
    font-size: 20px;
    color: #fff;
}

.info {
    display: flex;
    align-items: center;
    position: relative;
}

.info figure {
    margin-right: 0.8125rem;
}

.cross {
    position: absolute;
    width: 110px;
    /* height: 60px; */
    z-index: 4;
    right:10px;
     background: linear-gradient(270deg, #181818 53.65%, rgba(24, 24, 24, 0.8) 100%);
}
.cross figure{
text-align: center;
margin-left: 70px;
}
.twitter{
     background: #181818;
 transform: rotate(-4deg);
 position: absolute;
 left: 186px;
}
.pinterest{
       background: #181818;
    transform: rotate(2deg);
    position:absolute;
    left: 391px;
    top:70px;
}
.facebook{
       background: #181818;
    transform: rotate(-2deg);
    position: absolute;
    left: 647.12px;
}
.dribble{
       background: #181818;
transform: rotate(4deg);
position:absolute;
  top:70px;
left: 913.6px;

}.p-text{
    max-width: 180px;
}

@media screen and (max-width: 600px) {
    .facebook,.twitter,.dribble,.pinterest{
        position: static;
    }
}
</style>