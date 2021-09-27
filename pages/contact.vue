<template>
    <div>
        <MainMenu />
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