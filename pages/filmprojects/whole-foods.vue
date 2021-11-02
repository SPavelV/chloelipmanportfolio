<template>
    <LocomotiveScroll
        ref="scroller"
        :getted-options="{
        smooth: true,
        direction: 'vertical',
        smartphone: {
            //smooth: true,
            direction: 'vertical',
        },
        tablet: {
            //smooth: true,
            direction: 'vertical',
        },
        }"
    >
    <div class="white-menu">
        <section class="landing-filmproject-section">
            <h1>Whole Foods</h1>
            <div class="landing-iframe-container"><iframe src="https://player.vimeo.com/video/637255559?h=5f3e86f6e4&autoplay=1&loop=1&muted=1&color=ffffff&title=0&byline=0&portrait=0" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe><script src="https://player.vimeo.com/api/player.js"></script></div>
        </section>
        <section class="filmproject-details-section">
            <div class="filmproject-informations-container">
                <h2>Spec Commercial</h2>
                <h3><span>Director</span>/<span>Co-Dp</span>/<span>Editor</span></h3>
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/WholeFoods1.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/WholeFoods2.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/WholeFoods3.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/WholeFoods4.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/WholeFoods5.png" alt=""> 
            </div>
        </section>
    </div>
    </LocomotiveScroll>
</template>

<script>
export default {

}
</script>

<style lang="css" src="~/assets/css/main.css"></style>