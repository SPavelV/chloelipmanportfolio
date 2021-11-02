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
                        <a href="https://instagram.com/cllphoto_" target="_blank">Instagram</a>
                        <a href="https://www.linkedin.com/in/chloe-lipman/" target="_blank">Linkedin</a>
                    </div>
                </div>
            </div>
            <div class="contact-image-container">
                <img src="~/assets/img/menu-contact.jpeg" alt="">
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
            gsap.fromTo('#connect', 0.5, { opacity: 0, repeat: -1, repeatDelay: 10 },
            { opacity: 1, repeat: -1, repeatDelay: 10 });
            gsap.to('#connect', 0.5, { opacity: 0, delay: 3, repeat: -1, repeatDelay: 10 });
            
            gsap.fromTo('#create', 0.5, { opacity: 0, repeat: -1, repeatDelay: 10 },
            { opacity: 1, delay: 3.5, repeat: -1, repeatDelay: 10 });
            gsap.to('#create', 0.5, { opacity: 0, delay: 6.5, repeat: -1, repeatDelay: 10 });
            
            gsap.fromTo('#collaborate', 0.5, { opacity: 0, repeat: -1, repeatDelay: 10 },
            { opacity: 1, delay: 7, repeat: -1, repeatDelay: 10 });
            gsap.to('#collaborate', 0.5, { opacity: 0, delay: 10, repeat: -1, repeatDelay: 10 });
        },
    }

}
</script>

<style lang="css" src="~/assets/css/main.css"></style>