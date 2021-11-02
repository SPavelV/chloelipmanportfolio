<template>
  <div class="HomePage">
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
    <section class="landing-home-section" data-scroll-section data-scroll data-scroll-offset="0%, 0%" data-scroll-call="test" data-scroll-repeat>
        <div id="landing-home-section"></div>
        <div class="landing-home-container" data-scroll data-scroll-sticky data-scroll-target="#landing-home-section">
            <div class="landing-iframe-container"><iframe src="https://player.vimeo.com/video/631584056?h=20c4c25857&autoplay=1&loop=1&muted=1&color=ffffff&title=0&byline=0&portrait=0" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe><script src="https://player.vimeo.com/api/player.js"></script></div>
            <div class="landing-home-title-container" data-scroll data-scroll-direction="horizontal" data-scroll-speed="16.5">
                <prismic-rich-text :field="page.page_title" />
            </div>
        </div>
    </section>
    <section class="about-home-section" id="about" data-scroll-section>
        <div id="about-home-section"></div>
        <div class="about-home-container">
            <div class="storyteller-home-container" data-scroll data-scroll-call="AboutHomeAnimation">
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
        </div>
    </section>
    <section class="films-home-section" data-scroll-section>
        <div class="films-home-container">
            <prismic-rich-text :field="page.project_subtitle" data-scroll data-scroll-direction="horizontal" data-scroll-speed="6" />
        </div>
        <div class="filmprojects-home-container">
            <NuxtLink to="/filmprojects/the-perfect-match/" class="active">
                <prismic-rich-text :field="page.filmproject_name3" id="ThePerfectMatchLink"/>
                <prismic-image :field="page.filmproject_image_3" id="ThePerfectMatchImg"/>
            </NuxtLink>
            <NuxtLink to="/filmprojects/whole-foods/">
                <prismic-rich-text :field="page.filmproject_name1" id="WholeFoodsLink"/>
                <prismic-image :field="page.filmproject_image_1" id="WholeFoodsImg" />
            </NuxtLink>
            <NuxtLink to="/#">
                <prismic-rich-text :field="page.filmproject_name2" id="FloatingAwayLink"/>
                <prismic-image :field="page.filmproject_image_2" id="FloatingAwayImg" />
            </NuxtLink>
        </div>
        <div class="switch-all-project">
            <NuxtLink to="/film">
                All Project
            </NuxtLink>
        </div>
    </section>
    <section class="photo-home-section" data-scroll-section>
        <div class="films-home-container">
            <h2 data-scroll data-scroll-direction="horizontal" data-scroll-speed="6">Photography</h2>
        </div>
        <div class="photo-home-grid-container">
            <NuxtLink to="/photography/#0" class="photo-home-image-container">
                <prismic-image :field="page.photoproject_image_1" />
            </NuxtLink>
            <NuxtLink to="/photography/#1" class="photo-home-image-container">
                <prismic-image :field="page.photoproject_image_2" />
            </NuxtLink>
            <NuxtLink to="/photography/#2" class="photo-home-image-container">
                <prismic-image :field="page.photoproject_image_3" />
            </NuxtLink>
            <NuxtLink to="/photography/#15" class="photo-home-image-container">
                <prismic-image :field="page.photoproject_image_4" />
            </NuxtLink>
            <NuxtLink to="/photography/#14" class="photo-home-image-container">
                <prismic-image :field="page.photoproject_image_5" />
            </NuxtLink>
            <NuxtLink to="/photography/#8" class="photo-home-image-container">
                <prismic-image :field="page.photoproject_image_6" />
            </NuxtLink>
            <NuxtLink to="/photography/#6" class="photo-home-image-container">
                <prismic-image :field="page.photoproject_image_7" />
            </NuxtLink>
            <NuxtLink to="/photography/#4" class="photo-home-image-container">
                <prismic-image :field="page.photoproject_image_8" />
            </NuxtLink>
            <NuxtLink to="/photography/#18" class="photo-home-image-container">
                <prismic-image :field="page.photoproject_image_9" />
            </NuxtLink>
        </div>
    </section>
    <section class="contact-section home-contact" data-scroll-section>
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
                    <prismic-rich-text :field="page.contact_social_media_2" />
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
    </LocomotiveScroll>
  </div>
</template>

<script>
import { gsap } from "gsap";


export default {
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
        this.CalcWidthLandingText(),
        this.HoverProjects(),
        this.ListCaroussel(),
        this.ResponsiveValue()

        const locomotive = this.$refs.scroller.locomotive
        locomotive.on('call', (obj) => {
            if (obj === 'AboutHomeAnimation') {
                gsap.fromTo(".about-home-section h2", 1,{
                    translateX: "100%", opacity: 0
                },
                {   
                    translateX: "0%", opacity: 1
                })
                gsap.fromTo(".about-home-section h2", 1,{
                    opacity: 1
                },
                {   
                    opacity: 0.25, delay: 1
                })
                var AboutInfoWord = document.querySelectorAll(".about-infos-home-container .about-info-word-wrapper")
                gsap.fromTo(AboutInfoWord, 1,{
                    opacity: 0, translateY: 50,
                },
                {   
                    opacity: 1, translateY: 0, stagger: 0.25, delay: 1, 
                })

                var AboutInfoParagraphe = document.querySelector(".about-home-details-container .about-details-paragrapher p")
                gsap.fromTo(AboutInfoParagraphe, 1,{
                    opacity: 0, translateY: 50,
                },
                {   
                    opacity: 1, translateY: 0, delay: 1.25, 
                })

                var AboutInfoImage = document.querySelector(".about-home-details-container .about-details-image")
                gsap.fromTo(AboutInfoImage, 1,{
                    opacity: 0, translateY: "0%",
                },
                {   
                    opacity: 1, translateY: "-20%", delay: 1.5, 
                })
            }
            else if (obj === 'test') {
                var LogoContainer = document.querySelector('.logo-container a')
                var BurgerContainer = document.querySelector('.menu-open')
                LogoContainer.classList.toggle('black-logo')
                BurgerContainer.classList.toggle('black-burger')
            }
        });
    },

    methods: {
        CalcWidthLandingText: function(){
            var LandingText = document.querySelector(".landing-home-title-container")
            var WidthLandingText = LandingText.offsetWidth
            console.log(WidthLandingText)
        },
        HoverProjects: function(){
            var HomeProjectContainers = document.querySelectorAll(".filmprojects-home-container a")
            HomeProjectContainers.forEach( function(HomeProjectContainer){
                HomeProjectContainer.addEventListener("mouseenter", function() {
                    var HomeProjectCurrentContainer = document.querySelector(".filmprojects-home-container a.active")
                    HomeProjectCurrentContainer.classList.remove("active")
                    HomeProjectContainer.classList.add('active')
                })
            })
        },
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
