<template>
    <header :class=" { 'scrolled-nav' : scrollPosition}">
        <nav>
            <div class="branding">
               <img src="" alt="Apple logo">
            </div>
            <ul v-show="!mobile" class="navigation">
                <li><router-link class="link" :to="{name:'Home'}" >Home</router-link></li>
                <li><router-link class="link" :to="{name:''}" >Shop</router-link></li>
                <li><router-link class="link" :to="{name:'About'}" >About us</router-link></li>
                <li><router-link class="link" :to="{name:''}" >Contact</router-link></li>
            </ul>
                <div class="icon">
                    <i @click="teggleMobileNav" v-show="mobile" name="menu-outline" :class=" {'icon-active' : mobileNav}"></i>
                </div>
            <transition name="mobile-nav">
                <ul v-show="mobileNav" class="dropdown-nav">
                <li><router-link class="link" :to="{name:'Home'}" >Home</router-link></li>
                <li><router-link class="link" :to="{name:''}" >Shop</router-link></li>
                <li><router-link class="link" :to="{name:'About'}" >About us</router-link></li>
                <li><router-link class="link" :to="{name:''}" >Contact</router-link></li>
            </ul>
            </transition>
                
        </nav>
    </header>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
    
</style>