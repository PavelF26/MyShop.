<template>

    <header :class=" { 'scrolled-nav' : scrolledNav}">
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
                    <i @click="teggleMobileNav" v-show="mobile" class="far fa-bars" :class=" {'icon-active' : mobileNav}">
                    </i>
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
            scrolledNav:null,
            mobile:null,
            mobileNav:null,
            windowWidth:null,
        };
    },

    created(){
        window.addEventListener('resize', this.checkScreen);
        this.checkScreen();
    },

    updatedScroll(){

        const scrollPosition = window.scrollY;
        if(scrollPosition > 50){
            this.scrolledNav =true;
            return;
                            }
        this.scrolledNav = false;


    },
    mounted() {
        window.addEventListener('scroll', this.updatedScroll);
    },

    methods:{
        teggleMobileNav(){

            this.mobileNav = !this.mobileNav

        },


        checkScreen(){
            this.windowWidth = window.innerWidth;
            if(this.windowWidth <=750){
                this.mobile = true;
                return;
            }
            this.mobile = false;
            this.mobileNav = false;
            return;

        },

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
            &:hover{
                color: silver;
                
            }

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
            


        }

        .branding{
            display: flex;
            align-items: center;
            width: 11%;

            img{
                height: 100%;
                width: 63%;
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

        .dropdown-nav{
            display: flex;
            flex-direction: column;
            position: fixed;
            width: 100%;
            max-width: 250px;
            height: 100%;
            background-color: #fff;
            top: 0;
            left: 0;

            li{
                margin-left: 0;
                .link{
                    color: rgb(0,0,0,);
                }
            }
        }

        .mobile-nav-enter-active,
        .mobile-nav-leave-active {
             transition: 0.5s ease all;
        }

        .mobile-nav-enter-from,
        .mobile-nav-leave-to {
            transform: translateX(-250px) ;
        }

        .mobile-nav-enter-to{
            transform: translateX(0);
        }
        
        
    }

}

.scrolled-nav{
    background-color: #000;
    box-shadow: O 4px 6px -1px rgba(0,0,0,0.1), 0 2px 4px -1px  rgba(0,0,0,0.06);

    nav li{
        padding: 8px 0;

        .branding{
            width: 40px;
            box-shadow: O 4px 6px -1px rgba(0,0,0,0.1), 0 2px 4px -1px  rgba(0,0,0,0.06);

        }
    }

}


</style>
>>>>>>> navigation
