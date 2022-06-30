<template>
  <section class="section-one">
    <h2>Findtrend helps you to increase your <br/>
      productivity and reduce your computer's<br/>
      memory load, <span>an application that can <br/>
        fulfill your daily browsing needs.</span> </h2>
  </section>
  <section class="section-two">
    <h2 class="second-h2">Findtrend make +1000 Startup grow</h2>
    <div class="logo-grid">
        <div  v-for="image in images" :key="image.id">
        <div class="image-container">
             <figure><img :src="image.url" alt=""></figure>
    </div>
    </div>
    </div>
    
  </section>
</template>

<script>
export default {
    name:'SectionTwo',
    data(){
        return{
            images:[
                {id:'microsoft', url:require('@/assets/microsoft.svg')},
                {id:'allianz', url:require('@/assets/allianz.svg')},
                {id:'upwork', url:require('@/assets/upwork.svg')},
                {id:'volvo', url:require('@/assets/volvo.svg')},
                {id:'grab', url:require('@/assets/grab.svg')},
                {id:'verizon', url:require('@/assets/verizon.svg')},
                {id:'coinbase', url:require('@/assets/coinbase.svg')},
                {id:'expedia', url:require('@/assets/expedia.svg')},
                {id:'airtable', url:require('@/assets/airtable.svg')},
                {id:'magento', url:require('@/assets/magento.svg')},
                {id:'carrera', url:require('@/assets/carrera.svg')},
                {id:'bonanza', url:require('@/assets/bonanza.svg')},
                {id:'wetransfer', url:require('@/assets/wetransfer.svg')},
                {id:'suzuki', url:require('@/assets/suzuki.svg')},
                {id:'algolia', url:require('@/assets/algolia.svg')},
                {id:'heineken', url:require('@/assets/heineken.svg')},
                ]
        }
    }

}
</script>

<style scoped>
.section-one,.section-two {
  padding: 8.75rem;
  text-align: center;
}

.section-one h2,.section-two h2{
font-weight: 700;
font-size: 4rem;
line-height: 4.75rem;
}
.section-one span{
color: #ADADAD;
}
.image-container{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 16.625rem;
height: 7.5rem;
background: #F5F5F5;
border-radius: 8px;
}
.logo-grid{
    margin-top: 5rem;
    width: 100%;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    row-gap: 2rem;
    column-gap: normal;
}

@media screen and (max-width: 600px) {
  .section-two,.section-one{
    padding: 5rem 1.375rem;
  }
  .section-one h2,.section-two h2{
    font-size: 2.25rem;
    text-align: left;
    line-height: 2.6875rem;
  }
  .section-two h2{
    text-align: center;
  }
  .image-container{
    width: 100%;
    padding: 1.4375rem;
  }
  .image-container img{
    width: 100%;
  }
  .logo-grid{
    width: 100%;
    grid-template-columns: repeat(2, 1fr);
    gap: 0.9375rem;
  }
}
</style>