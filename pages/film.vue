<template>
    <div class="white-menu">
        <MainMenu />
        <section class="film-page-section">
            <NuxtLink class="page-film-container" to="/">
                <h2>Whole Foods</h2>
                <img src="~/assets/img/1Floating.jpg" alt="">
            </NuxtLink>
            <NuxtLink class="page-film-container" to="/">
                <h2>Floating Away</h2>
                <img src="~/assets/img/8Emily.jpg" alt="">
            </NuxtLink>
            <NuxtLink class="page-film-container" to="/">
                <h2>The Perfect Match</h2>
                <img src="~/assets/img/17SorrentoLandscape.jpg" alt="">
            </NuxtLink>
        </section>
    </div>
</template>

<script>
import MainMenu from '@/components/MainMenu'

export default {

    components: { MainMenu }

}
</script>

<style lang="css" src="~/assets/css/main.css"></style>