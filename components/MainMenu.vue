<template>
    <header>
        <div class="logo-container">
            <NuxtLink to="/"><img class="logo-image" src="#" alt="Logo Chloe Lipman"></NuxtLink>
        </div>

        <div class="menu-area">
            <input class="menu-btn" type="checkbox" />
            <label for="menu-toggle" class="menu-open">
                <div id="open" class="menu-burger"></div>
            </label>
            <div class="menu menu-effects">
                <label for="menu-toggle"></label>
                <div class="menu-content">
                    <ul>
                        <li>
                            <nuxt-link to="/about">About</nuxt-link>
                            <img src="" alt="">
                        </li>
                        <li>
                            <nuxt-link to="/films">Films</nuxt-link>
                            <img src="" alt="">
                        </li>
                        <li>
                            <nuxt-link to="/photography">Photography</nuxt-link>
                            <img src="" alt="">
                        </li>
                        <li>
                            <nuxt-link to="/contact">Contact</nuxt-link>
                            <img src="" alt="">
                        </li>
                    </ul>
                </div>
                <div class="sub-menu">
                    <div class="legal-mention">
                        <p class="credit">
                            <span>Chloe Lipman © 2021</span>
                            <span>All Rights Reserved</span>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </header>
  </template>
  
  <script>
  export default {

  }
  </script>