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
            <h1>Floating Away</h1>
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
    </LocomotiveScroll>
</template>

<script>
export default {

}
</script>

<style lang="css" src="~/assets/css/main.css"></style>