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
        <section class="film-page-section">
             <NuxtLink class="page-film-container active" to="/filmprojects/the-perfect-match/" data-scroll-section>
                <h2 class="active">The Perfect Match</h2>
                <img src="~/assets/img/17SorrentoLandscape.jpg" alt="">
            </NuxtLink>
            <NuxtLink class="page-film-container" to="/filmprojects/whole-foods/" data-scroll-section>
                <h2>Whole Foods</h2>
                <img src="~/assets/img/1Floating.jpg" alt="">
            </NuxtLink>
            <NuxtLink class="page-film-container" to="#" data-scroll-section>
                <h2>Floating Away</h2>
                <img src="~/assets/img/8Emily.jpg" alt="">
            </NuxtLink>
        </section>
    </div>
    </LocomotiveScroll>
</template>

<script>
export default {

    mounted: function(){
        this.HoverProjects()
    },

    methods: {
        HoverProjects: function(){
            var FilmContainers = document.querySelectorAll(".page-film-container")
            FilmContainers.forEach( function(FilmContainer){
                FilmContainer.addEventListener("mouseenter", function() {
                    var FilmCurrentContainer = document.querySelector(".page-film-container.active")
                    FilmCurrentContainer.classList.remove("active")

                    var FilmCurrentTitle = document.querySelector(".page-film-container h2.active")
                    FilmCurrentTitle.classList.remove("active")
                    
                    FilmContainer.classList.add("active")

                    var FilmTitle = document.querySelector(".page-film-container.active h2")
                    FilmTitle.classList.add("active")
                })
            })
        }
    }

}
</script>

<style lang="css" src="~/assets/css/main.css"></style>