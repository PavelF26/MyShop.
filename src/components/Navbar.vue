<template>
    <header :class=" { 'scrolled-nav' : scrollPosition}">
        <nav>
            <div class="branding">
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

header{
    background-color: rgba(0,0,0,0.8);
    z-index: 99;
    width: 100%;
    position: fixed;
    transition: .5s ease all ;
    color: #fff;
    

    nav{
        display: flex;
        flex-direction: row;
        padding: 12px 0;
        transition: .5s ease all ;
        width: 90%;
        margin: 0 auto;
        /*12:25*/

        
    }

}

    
</style>