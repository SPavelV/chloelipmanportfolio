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
            <h1>The Perfect Match</h1>
            <img src="~/assets/img/ThePerfectMatch1.png" alt="">
        </section>
        <section class="filmproject-details-section">
            <div class="filmproject-informations-container">
                <h2>Spec Commercial</h2>
                <h3><span>Director</span>/<span>Co-Dp</span>/<span>Editor</span></h3>
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/ThePerfectMatch2.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/ThePerfectMatch3.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/ThePerfectMatch4.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/ThePerfectMatch5.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/ThePerfectMatch6.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/ThePerfectMatch7.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/ThePerfectMatch8.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/ThePerfectMatch9.png" alt=""> 
            </div>
            <div class="filmproject-image-container">
                <img src="~/assets/img/ThePerfectMatch10.png" alt=""> 
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