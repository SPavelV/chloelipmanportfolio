<template>
    <div class="white-menu">
        <MainMenu />
        <section class="landing-filmproject-section">
            <h1>Whole Foods</h1>
            <img src="~/assets/img/1Floating.jpg" alt="">
        </section>
        <section class="filmproject-details-section">
            <div class="filmproject-informations-container">
                <h2>Spec Commercial</h2>
                <h3><span>Director</span>/<span>Co-Dp</span>/<span>Editor</span></h3>
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/1Floating.jpg" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/1Floating.jpg" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/1Floating.jpg" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/1Floating.jpg" alt=""> 
            </div>
        </section>
    </div>
</template>

<script>
import MainMenu from '@/components/MainMenu'

export default {

    components: { MainMenu }

}
</script>

<style lang="css" src="~/assets/css/main.css"></style>