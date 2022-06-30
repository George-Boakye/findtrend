<template>
  <footer>
    <figure>
        <img src="@/assets/logo-dark.svg" alt="">
    </figure>
    <div>
        <a href="">Privacy Policy</a>
        <a href="">Terms and Conditions</a>
        <a href="">Contact Us</a>
        <a href="">Careers</a>
    </div>
  </footer>
</template>

<script>
export default {
name:'Footer'
}
</script>

<style scoped>
footer{
    background-color: #fff;
    padding: 1.875rem 5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;

}
a{
text-decoration: none;
color: #000;
margin-right: 2.5rem;
font-weight: 400;
font-size: 1.125rem;
line-height: 100%;
}
@media screen and (max-width: 600px) {
    footer{
        padding: 3.875rem;
        flex-direction: column;
        text-align: center;
    }
    footer div{
        margin-top: 6.6875rem;
    }
    a{
        display: block;
        margin-right: 0;
        margin-bottom: 2.5rem;
    }
}
</style>