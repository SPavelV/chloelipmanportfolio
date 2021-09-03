<template>
    <div>
        <MainMenu />
        <div>
            <NuxtLink to="/">
                <div>
                    <h2>Whole Foods</h2>
                </div>
                <img src="" alt="">
            </NuxtLink>
            <NuxtLink to="/">
                <div>
                    <h2>Floating Away</h2>
                </div>
                <img src="" alt="">
            </NuxtLink>
            <NuxtLink to="/">
                <div>
                    <h2>The Perfect Match</h2>
                </div>
                <img src="" alt="">
            </NuxtLink>
        </div>
    </div>
</template>

<script>
import MainMenu from '@/components/MainMenu'

export default {

    components: { MainMenu }

}
</script>

<style></style>