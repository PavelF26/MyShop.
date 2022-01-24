<template>
    <header :class=" { 'scrolled-nav' : scrollPosition}">
        <nav>
            <div class="branding">
                <img src="../assets/img/apple-logo.jpeg" alt="">
            </div>
            <ul v-show="!mobile" class="navigation">
                <li><router-link class="link" :to="{name:'Home'}" >Home</router-link></li>
                <li><router-link class="link" :to="{name:''}" >Shop</router-link></li>
                <li><router-link class="link" :to="{name:'About'}" >About us</router-link></li>
                <li><router-link class="link" :to="{name:''}" >Contact</router-link></li>
            </ul>
                <div class="icon">
                    <ion-icon @click="teggleMobileNav" v-show="mobile" name="menu-outline" :class=" {'icon-active' : mobileNav}"></ion-icon>
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
    name:"navigation",
    data() {
        return {
            scrollPosition:null,
            mobile:null,
            mobileNav:null,
            windowWidth:null,
        };
    },
    
};
</script>

<style lang="scss" scoped>

header{
    background-color: rgb(0,0,0,);
    z-index: 99;
    width: 100%;
    position: fixed;
    transition: 0.5s ease all ;
    color: #fff;
    top: 0;
    left: 0;
    

    nav{
        position: relative;
        display: flex;
        flex-direction: row;
        padding: 12px 0;
        transition: .5s ease all ;
        width: 90%;
        margin: 0 auto;
        @media (min-width: 1140px) {
            max-width:1140px ;
            
        }
        ul,
        .link{ 
            font-weight: 500;
            color: #fff;
            list-style: none;
            text-decoration: none;

        }

        li{
            text-transform: uppercase;
            /*padding: 16px;*/
            margin-left: 16px;
        }
        .link{
            font-size: 14px;
            padding-bottom: 5px;
            transition: 0.5s ease all ;
            border-bottom: 1px solid transparent;
            &:hover{
                color: silver;
                border-color: silver;
            }


        }

        .branding{
            display: flex;
            align-items: center;
            width: 10%;

            img{
                height: 65%;
                width: 50%;
                transition: 0.5s ease all ;


            }

        }

        .navigation{
            display: flex;
            align-items: center;
            flex: 1;
            justify-content: flex-end;


        }


        .icon{
            display: flex;
            align-items: center;
            position: absolute;
            top: 0;
            right: 24px;
            height: 100%;
            

            i{
                cursor: pointer;
                font-size: 24px;
                transition: .8s ease all;

            }

        }
        .icon-active{
            transform: rotate(180deg);
        }
        
    }

    /*20:53*/

}

</style>