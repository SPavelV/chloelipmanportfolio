<template>
  <div>
    <MainMenu />
    <section class="landing-home-section">
        <div class="landing-home-title-container">
            <h1>Chloe Lipman</h1>
        </div>
        <img src="~/assets/img/8Emily.jpg" alt="">
    </section>
    <section class="about-home-section" id="about">
        <div class="storyteller-home-container">
            <h2>Storyteller</h2>
        </div>
        <div class="about-infos-home-container">
            <div class="about-info-word-wrapper">
                <h3>Cinematographer</h3>
            </div>
            <div class="about-info-word-wrapper">
                <h3>Director</h3>
            </div>
            <div class="about-info-word-wrapper">
                <h3>Photographer</h3>
            </div>
        </div>
        <div class="about-home-details-container">
            <div class="about-details-paragrapher">
                <p>Chloe Lipman is visual artist and impassioned filmaker based in New York City. She is a recent graduate from NYU Tisch School of the arts with a B.F.A in film and television production.</p>
            </div>
            <div class="about-details-image">
                <img src="~/assets/img/8Emily.jpg" alt="">
            </div>
        </div>
    </section>
    <section class="films-home-section">
        <div class="films-home-container">
            <h2>Selected Work</h2>
        </div>
        <div class="filmprojects-home-container">
            <NuxtLink to="/">
                <h2>Whole Foods</h2>
            </NuxtLink>
            <NuxtLink to="/">
                <h2>Floating Away</h2>
            </NuxtLink>
            <NuxtLink to="/">
                <h2>The Perfect Match</h2>
            </NuxtLink>
            <img src="~/assets/img/1Floating.jpg" alt="">
            <img src="~/assets/img/8Emily.jpg" alt="">
            <img src="~/assets/img/17SorrentoLandscape.jpg" alt="">
            <div class="switch-all-project">
                <NuxtLink to="/film">
                    All Project
                </NuxtLink>
            </div>
        </div>
    </section>
    <section class="photo-home-section">
    <div class="photo-home-grid-container">
        <NuxtLink to="/photography/#photo1" class="photo-home-image-container">
            <img src="~/assets/img/1Floating.jpg" alt="">
        </NuxtLink>
        <NuxtLink to="/photography/#photo2" class="photo-home-image-container">
            <img src="~/assets/img/2CamrynBed.jpg" alt="">
        </NuxtLink>
        <NuxtLink to="/photography/#photo3" class="photo-home-image-container">
            <img src="~/assets/img/3AmalfiMountains.jpg" alt="">
        </NuxtLink>
        <NuxtLink to="/photography/#photo4" class="photo-home-image-container">
            <img src="~/assets/img/4DoubleExposure.jpg" alt="">
        </NuxtLink>
        <NuxtLink to="/photography/#photo5" class="photo-home-image-container">
            <img src="~/assets/img/5Cassie.jpg" alt="">
        </NuxtLink>
        <NuxtLink to="/photography/#photo6" class="photo-home-image-container">
            <img src="~/assets/img/6CamrynPortrait.jpg" alt="">
        </NuxtLink>
        <NuxtLink to="/photography/#photo7" class="photo-home-image-container">
            <img src="~/assets/img/7SpainStreets.jpg" alt="">
        </NuxtLink>
        <NuxtLink to="/photography/#photo8" class="photo-home-image-container">
            <img src="~/assets/img/8Emily.jpg" alt="">
        </NuxtLink>
        <NuxtLink to="/photography/#photo9" class="photo-home-image-container">
            <img src="~/assets/img/9SunsetTwinkle.jpg" alt="">
        </NuxtLink>
    </div>
    </section>
    <section class="contact-section">
        <div class="contact-infos-container">
            <div class="contact-title-container">
                <div>
                    <h1>Let's</h1>
                </div>
                <div class="contact-words-slider">
                    <div v-for="contactlistitem in contactlistitems" :key="contactlistitem.id" class="contact-list-item" :id="contactlistitem.id"><h1>{{ contactlistitem.word }}</h1></div>
                </div>          
            </div>
            <div class="contact-infos-wrapper">
                <div class="contact-infos-colums">
                    <h2>Contact</h2>
                    <a href="mailto:clipman@gmail.com">clipman17@gmail.com</a>
                </div>
                <div class="contact-follows-colums">
                    <h2>Follow</h2>
                    <a href="#instagram">Instagram</a>
                    <a href="#linkedin">Linkedin</a>
                </div>
            </div>
        </div>
        <div class="contact-image-container">
            <img src="~/assets/img/6CamrynPortrait.jpg" alt="">
        </div>
        <div class="legal-mention-container">
            <p>Chloe Lipman © 2021</p>
            <p>All Rights Reserved</p>
        </div>
    </section>
  </div>
</template>

<script>
import MainMenu from '@/components/MainMenu'
import { gsap } from "gsap";

export default {

    components: { MainMenu },

    data: () => ({
        contactlistitems: [
            {
                word: 'Connect',
                id:'connect'
            },
            {
                word: 'Create',
                id:'create'
            },
            {
                word: 'Collaborate',
                id:'collaborate'
            }
        ]
    }),

    mounted: function(){
        this.ListCaroussel()
    },

    methods: {
        ListCaroussel: function(){
            
            gsap.fromTo('#connect', 1, { opacity: 0, repeat: -1, repeatDelay: 17 },
            { opacity: 1, repeat: -1, repeatDelay: 17 });
            gsap.to('#connect', 1, { opacity: 0, delay: 5, repeat: -1, repeatDelay: 17 });
            
            gsap.fromTo('#create', 1, { opacity: 0, repeat: -1, repeatDelay: 17 },
            { opacity: 1, delay: 6, repeat: -1, repeatDelay: 17 });
            gsap.to('#create', 1, { opacity: 0, delay: 11, repeat: -1, repeatDelay: 17 });
            
            gsap.fromTo('#collaborate', 1, { opacity: 0, repeat: -1, repeatDelay: 17 },
            { opacity: 1, delay: 12, repeat: -1, repeatDelay: 17 });
            gsap.to('#collaborate', 1, { opacity: 0, delay: 17, repeat: -1, repeatDelay: 17 });
        }
    }
}
</script>

<style lang="css" src="~/assets/css/main.css"></style>