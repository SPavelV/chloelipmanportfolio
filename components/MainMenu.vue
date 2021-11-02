<template>
    <header class="header">
		<div class="logo-container">
			<NuxtLink class="home-logo" id="site-logo" to="/"><img src="~/assets/img/ChloeLogo.png" alt="logo Chloe Lipman"></NuxtLink>
		</div>

		<div class="menu-area">
			<input type="checkbox" id="menu-toggle">
			<label for="menu-toggle" class="menu-open">
				<div id="open" class="menu-burger"></div>
			</label>
			<div class="menu menu-effects">
				<label for="menu-toggle"></label>
				<div class="menu-content">
                    <ul>
                        <li>
                            <NuxtLink to="/">About</NuxtLink>
                            <img src="~/assets/img/menu-about.jpeg" alt="">
                        </li>
                        <li>
                            <NuxtLink to="/film">Films</NuxtLink>
                            <img src="~/assets/img/WholeFoods2.png" alt="">
                        </li>
                        <li>
                            <NuxtLink to="/gridphotography">Photography</NuxtLink>
                            <img src="~/assets/img/1Floating.jpg" alt="">
                        </li>
                        <li>
                            <NuxtLink to="/contact">Contact</NuxtLink>
                            <img src="~/assets/img/menu-contact.jpeg" alt="">
                        </li>
                    </ul>
				</div>
			</div>
		</div>
	</header>
</template>
  
<script>
export default {
    mounted: function(){
        this.OpenMenuAnimation(),
        this.ResponsiveHeightValue()
    },

    methods: {
        OpenMenuAnimation: function(){
            var menuToggle = document.getElementById('menu-toggle');
            var menuLogo = document.getElementById('site-logo');
            var menuBurger = document.querySelector('.menu-open');
            var menuLinks = document.querySelectorAll('.menu-content a')

            menuToggle.addEventListener("click", function(){ 
                menuLogo.classList.toggle("menu-active")
                menuBurger.classList.toggle("menu-active")
            })

            menuLinks.forEach(function(menuLink){
                menuLink.addEventListener("click", function(){ 
                    menuLogo.classList.remove("menu-active")
                    menuBurger.classList.remove("menu-active")
                    menuLogo.classList.remove("black-logo")
                    menuBurger.classList.remove("black-burger")
                    document.getElementById("menu-toggle").checked = false;
                })
            })

        },
        ResponsiveHeightValue: function(){
            document.querySelector(':root').style
            .setProperty('--vh', window.innerHeight/100 + 'px');
        },
    }
}
</script>

<style lang="css" src="~/assets/css/main.css"></style>