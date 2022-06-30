<template>
    <section>
        <h2>Get your best deal</h2>
        <div class="subscribtion">
            <div class="text">
                <p>Monthly</p>
            </div>
            <div class="switch">
                <RoundedSwitch />
            </div>
            <div class="text">
                <p class="yearly">Yearly</p>
            </div>
            <figure><img class="desktop-arrow" src="@/assets/save-ten.svg" alt="">
                <img class="mobile-arrow" src="@/assets/save-ten-mobile.svg" alt="">
            </figure>
        </div>
        <div class="card-container">
            <div class="card" :class="card.type" v-for="(card) in data" :key="card.id">
                <div class="card-header">
                    <h4>{{ card.type }}</h4>
                    <p>{{ card.info }}</p>
                </div>
                <div>
                    <h3>${{ card.price }}<span>/Month</span></h3>
                    <ul v-for="item in card.list" :key="item">
                        <li>
                            <figure class="stroke"><img src="@/assets/stroke.svg" alt=""></figure> {{ item }}
                        </li>
                    </ul>
                </div>
                <Button text="Start Free Trial" />
            </div>
        </div>
    </section>
    <div class="lower-sec">
        <h1>
            Join us on email for <br>
            <span> more trending topics</span>
        </h1>
        <Button text="Join Now" :style="{ 'background-color': '#000' }" />
    </div>
</template>

<script>
import Button from '@/components/Button.vue'
import Switch from '@/components/RoundedSwitch.vue'
import RoundedSwitch from '@/components/RoundedSwitch.vue'
export default {
    name: 'SectionFour',
    components: {
        Button,
        Switch,
        RoundedSwitch
    },
    data() {
        return {
            data: [
                { id: '1', type: 'Personal', info: 'Special first packet for all', price: 8, list: ['Up to 5 page each group', 'Up to 10 group page', '5 Days group page saved'] },
                { id: '2', type: 'Regular', info: 'Recommended for personal pro', price: 20, list: ['Up to 15 page each group', 'Download page up to 20 page', 'Up to 10 group page', '15 Days group page saved'] },
                { id: '3', type: 'Premium', info: 'Packet for Startup & Company', price: 48, list: ['Unlimited group pages', 'Unlimited download page', 'Unlimited page each group', 'Customize sorting group pages', 'Customize group page name', '30 Days group page saved'] },
            ]
        }
    },
    methods: {
        changeColor(value) {

        }
    }
}
</script>

<style scoped>
section {
    padding: 8.75rem;
    background-color: #000;
    color: #fff;
    text-align: center;
}

h1 {
    font-weight: 900;
    font-size: 72px;
    line-height: 112%;
}

h2 {
    font-weight: 700;
    font-size: 4rem;
    line-height: 4.75rem;
}

h3 {
    font-weight: 400;
    font-size: 64px;
    line-height: 100%;
    margin-bottom: 2.125rem;
}

span {
    font-weight: 400;
    font-size: 18px;
    line-height: 100%;
}

h4 {
    font-weight: 400;
    font-size: 2.25rem;
    line-height: 100%;
    margin-bottom: 0.5rem;
}

p {
    font-weight: 400;
    font-size: 18px;
    line-height: 100%;
    margin-bottom: 2rem;
}

li {
    margin-bottom: 1.875rem;
    font-weight: 400;
    font-size: 18px;
    line-height: 100%;
    list-style: none;
}

.mobile-arrow {
    display: none;
}

.stroke {
    display: inline;
    margin-right: 13px;
}

.card {
    padding: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    width: 360px;
    height: 640px;
    color: #000;
    background: #FAFAFA;
    border-radius: 16px;

}

.card-container {
    text-align: left;
    margin-top: 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.card-header {
    border-bottom: 1px solid #000;
}

Button {
    width: 296px;
    height: 58px;
    background: #A8FF35;
    border-radius: 1.8125rem;
    border: none;
}

.Regular {
    background-color: #A8FF35;
}

.Regular button {
    background-color: #000;
    color: #fff;
}

.lower-sec {
    text-align: center;
    padding: 8.75rem 21.875rem;
    background: #A8FF35;
}

.lower-sec span {
    font-weight: 900;
    font-size: 72px;
    line-height: 112%;
    opacity: 0.3;
}

.lower-sec Button {
    margin-top: 40px;
    color: #fff;
    width: 180px;
}

.subscribtion {
    display: flex;
    justify-content: center;
    align-items: center;
}

.text p {
    margin-bottom: 0;
    margin-right: 1.5rem;
    margin-left: 1.5rem;
}

.switch {
    display: flex;
    justify-content: space-between;
}

@media screen and (max-width: 600px) {
    section {
        padding: 5rem 1.125rem;
    }

    h2 {
        font-weight: 900;
        font-size: 2.25rem;
        line-height: 43px;
    }

    .card-container {
        flex-direction: column;
    }

    .card {
        margin-bottom: 1.5rem;
    }

    .lower-sec {
        padding: 5rem 1.125rem;
    }

    .lower-sec span {
        font-weight: 900;
        font-size: 36px;
        line-height: 112%;
    }

    .mobile-arrow {
        display: block;
        position: relative;
        top: 40px;
        right: 100px;
    }

    .desktop-arrow {
        display: none;
    }

    .subscribtion {
        margin: 0 auto;
    }

    .yearly {
        color: #F5F5F5;
        opacity: 0.5;
    }
}
</style>