<template>
    <div>
        <MainMenu />
        <section class="photography-section">
            <div class="slides-inner">
                <div class="slide">
                    <img id="photo1" src="~/assets/img/1Floating.jpg" alt="">
                </div>
                <div class="slide">
                    <img id="photo2" src="~/assets/img/2CamrynBed.jpg" alt="">
                </div>
                <div class="slide">
                    <img id="photo3" src="~/assets/img/6CamrynPortrait.jpg" alt="">
                </div>
                <div class="slide">
                    <img id="photo4" src="~/assets/img/8Emily.jpg" alt="">
                </div>
                <div class="slide">
                    <img id="photo5" src="~/assets/img/11SorrentoWindow.jpg" alt="">
                </div>
                <div class="slide">
                    <img id="photo6" src="~/assets/img/17SorrentoLandscape.jpg" alt="">
                </div>
            </div>
            <button class="home-arrows" id="prev"><svg xmlns="http://www.w3.org/2000/svg" width="3vw" height="3vw" viewBox="0 0 376.874 595.49"><g id="right-thin-arrow-angle" transform="translate(0 0)"><g id="Groupe_46" data-name="Groupe 46" transform="translate(0 0)"><path id="Tracé_10" data-name="Tracé 10" d="M394.467,595.49c3.457,0,6.817-2.472,8.67-6.894,2.762-6.592,1.123-15.019-3.66-18.826L57.6,297.745,399.477,25.72c4.783-3.807,6.422-12.234,3.66-18.826s-8.876-8.852-13.66-5.044L32.6,285.811c-3.094,2.461-5,7.012-5,11.935s1.906,9.474,5,11.935L389.477,593.641A7.97,7.97,0,0,0,394.467,595.49Z" transform="translate(-27.604 0)" fill="#fff"/></g></g></svg></button>
            <button class="home-arrows" id="next"><svg xmlns="http://www.w3.org/2000/svg" width="3vw" height="3vw" viewBox="0 0 376.875 595.49"><g id="right-thin-arrow-angle" transform="translate(-27.604 0)"><g id="Groupe_46" data-name="Groupe 46" transform="translate(27.604 0)"><path id="Tracé_10" data-name="Tracé 10" d="M37.616,595.49c-3.457,0-6.817-2.472-8.67-6.894-2.762-6.592-1.123-15.019,3.66-18.826L374.479,297.745,32.606,25.72c-4.783-3.807-6.422-12.234-3.66-18.826s8.876-8.852,13.66-5.044L399.479,285.811c3.094,2.461,5,7.012,5,11.935s-1.906,9.474-5,11.935L42.606,593.641A7.97,7.97,0,0,1,37.616,595.49Z" transform="translate(-27.604 0)" fill="#fff"/></g></g></svg></button>
            <div class="project-gridbtn-container">
                <NuxtLink to="/gridphotography">
                    <svg xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 19 19">
                        <g id="Groupe_11" data-name="Groupe 11" transform="translate(-178 -599)">
                        <rect id="Rectangle_11" data-name="Rectangle 11" width="3" height="3" transform="translate(178 615)" fill="#fff"/>
                        <rect id="Rectangle_14" data-name="Rectangle 14" width="3" height="3" transform="translate(178 607)" fill="#fff"/>
                        <rect id="Rectangle_17" data-name="Rectangle 17" width="3" height="3" transform="translate(178 599)" fill="#fff"/>
                        <rect id="Rectangle_12" data-name="Rectangle 12" width="3" height="3" transform="translate(186 615)" fill="#fff"/>
                        <rect id="Rectangle_15" data-name="Rectangle 15" width="3" height="3" transform="translate(186 607)" fill="#fff"/>
                        <rect id="Rectangle_18" data-name="Rectangle 18" width="3" height="3" transform="translate(186 599)" fill="#fff"/>
                        <rect id="Rectangle_13" data-name="Rectangle 13" width="3" height="3" transform="translate(194 615)" fill="#fff"/>
                        <rect id="Rectangle_16" data-name="Rectangle 16" width="3" height="3" transform="translate(194 607)" fill="#fff"/>
                        <rect id="Rectangle_19" data-name="Rectangle 19" width="3" height="3" transform="translate(194 599)" fill="#fff"/>
                        </g>
                    </svg>
                </NuxtLink>
            </div>
        </section>
    </div>
</template>

<script>
import MainMenu from '@/components/MainMenu'

import $ from 'jquery'
import 'slick-carousel-latest'

window.jQuery = window.$ = $; 


export default {

    components: { MainMenu },

    mounted: function() {
        this.sliderAnimation()
    },

    methods: {
        sliderAnimation: function() {
            $('.slides-inner').slick({
                centerMode: true,
                centerPadding: '60px',
                slidesToShow: 3,
                variableWidth: true,
                prevArrow: $('#prev'),
                nextArrow: $('#next')
            });
        }
    }

}
</script>

<style lang="css" src="~/assets/css/main.css"></style>