<template>
  <div>
    <MainMenu />
    <section class="landing-home-section">
        <div class="landing-home-title-container">
             <prismic-rich-text :field="page.page_title" />
        </div>
        <div v-if="is_not_responsive" style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/631584056?h=20c4c25857&autoplay=1&loop=1&muted=1&color=ffffff&title=0&byline=0&portrait=0" style="position:absolute;top:-20vh;left:-10vw;width:120vw;height:140vh;" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
        <div v-if="is_responsive" style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/631584056?h=20c4c25857&autoplay=1&loop=1&muted=1&color=ffffff&title=0&byline=0&portrait=0" style="position:absolute;top:-10vh;left:-170vw;width:440vw;height:120vh;" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
    </section>
    <section class="about-home-section" id="about">
        <div class="storyteller-home-container">
            <prismic-rich-text :field="page.subtitle_about" />
        </div>
        <div class="about-infos-home-container">
            <div class="about-info-word-wrapper">
                <prismic-rich-text :field="page.key_words_about1" />
            </div>
            <div class="about-info-word-wrapper">
                <prismic-rich-text :field="page.key_words_about2" />
            </div>
            <div class="about-info-word-wrapper">
                <prismic-rich-text :field="page.key_words_about3" />
            </div>
        </div>
        <div class="about-home-details-container">
            <div class="about-details-paragrapher">
                <prismic-rich-text :field="page.about_paragraph" />
            </div>
            <div class="about-details-image">
                <prismic-image :field="page.image_about" />
            </div>
        </div>
    </section>
    <section class="films-home-section">
        <div class="films-home-container">
            <prismic-rich-text :field="page.project_subtitle" />
        </div>
        <div class="filmprojects-home-container">
            <NuxtLink to="/">
                <prismic-rich-text :field="page.filmproject_name1" />
            </NuxtLink>
            <NuxtLink to="/">
                <prismic-rich-text :field="page.filmproject_name2" />
            </NuxtLink>
            <NuxtLink to="/">
                <prismic-rich-text :field="page.filmproject_name3" />
            </NuxtLink>
            <prismic-image :field="page.filmproject_image_1" />
            <prismic-image :field="page.filmproject_image_2" />
            <prismic-image :field="page.filmproject_image_3" />
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
            <prismic-image :field="page.photoproject_image_1" />
        </NuxtLink>
        <NuxtLink to="/photography/#photo2" class="photo-home-image-container">
            <prismic-image :field="page.photoproject_image_2" />
        </NuxtLink>
        <NuxtLink to="/photography/#photo3" class="photo-home-image-container">
            <prismic-image :field="page.photoproject_image_3" />
        </NuxtLink>
        <NuxtLink to="/photography/#photo4" class="photo-home-image-container">
            <prismic-image :field="page.photoproject_image_4" />
        </NuxtLink>
        <NuxtLink to="/photography/#photo5" class="photo-home-image-container">
            <prismic-image :field="page.photoproject_image_5" />
        </NuxtLink>
        <NuxtLink to="/photography/#photo6" class="photo-home-image-container">
            <prismic-image :field="page.photoproject_image_6" />
        </NuxtLink>
        <NuxtLink to="/photography/#photo7" class="photo-home-image-container">
            <prismic-image :field="page.photoproject_image_7" />
        </NuxtLink>
        <NuxtLink to="/photography/#photo8" class="photo-home-image-container">
            <prismic-image :field="page.photoproject_image_8" />
        </NuxtLink>
        <NuxtLink to="/photography/#photo9" class="photo-home-image-container">
            <prismic-image :field="page.photoproject_image_9" />
        </NuxtLink>
    </div>
    </section>
    <section class="contact-section home-contact">
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
                    <prismic-rich-text :field="page.contact_mail" />
                </div>
                <div class="contact-follows-colums">
                    <h2>Follow</h2>
                    <prismic-rich-text :field="page.contact_social_media_1" />
                    <prismic-rich-text :field="page.contact_social_media_1" />
                </div>
            </div>
        </div>
        <div class="contact-image-container">
            <prismic-image :field="page.contact_image" />
        </div>
        <div class="legal-mention-container">
            <prismic-rich-text :field="page.legal_mention_name_and_date" />
            <p>All Rights Reserved</p>
        </div>
    </section>
  </div>
</template>

<script>
import MainMenu from '@/components/MainMenu'
import { gsap } from "gsap"

export default {
    components: { MainMenu },

    name: 'HomePage',

    async asyncData({ $prismic, error }) {
        try {
        const pageContent = (await $prismic.api.getSingle('my_test_page')).data
        return {
            page: pageContent
        }
        } catch (e) {
        error({ statusCode: 404, message: 'Page not found' })
        }
    },

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
        ],
        page: null,
        is_not_responsive: true,
        is_responsive: false,
    }),

    mounted: function(){
        this.ListCaroussel(),
        this.ResponsiveValue()
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
        },
        ResponsiveValue: function(){
            const that = this 
            console.log(that.is_not_responsive)
            console.log(that.is_responsive)
            var element = document.querySelector('.landing-home-section');
            var style = window.getComputedStyle(element);
            var margin = style.getPropertyValue('margin-bottom');

            if ( margin === "200px"){
                that.is_not_responsive = false
                that.is_responsive = true
                console.log(that.is_not_responsive)
                console.log(that.is_responsive)
            }
            else{
                that.is_not_responsive = true
                that.is_responsive = false
                console.log(that.is_not_responsive)
                console.log(that.is_responsive)
            }
        }
    }
}
</script>

<style lang="css" src="~/assets/css/main.css"></style>
