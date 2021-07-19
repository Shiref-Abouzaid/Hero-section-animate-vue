<template>
    <nav class="nav" :class="{'show': sideBarIsShow}">
        <div class="container d-flex">
            <div class="brand" >
                <template v-if="!sideBarIsShow">
                    <img src="@/assets/images/icons/outdoor.png" alt="menu" class="logo">
                    <div class="brand-name">Hiking</div>
                </template>
            </div>
            <div class="menu">
                <div class="menu-icon" @click="sideBarIsShow = !sideBarIsShow">
                    <!-- <img src="@/assets/images/icons/menu.png" alt="menu"> -->
                    <span></span>
                </div>
            </div>
        </div>
        <div class="d-flex side-bar-container">
            <div class="navegation-bar-animation-bg"></div>
            <div class="navegation-bar-overlay" v-if="sideBarIsShow" @click="sideBarIsShow = false"></div>
            <div class="sibe-bar-header">
                <div class="brand">
                    <img src="@/assets/images/icons/outdoor.png" alt="menu" class="logo">
                    <div class="brand-name">Hiking</div>
                </div>
            </div>
            <div class="side-bar">
                <ul class="list-container">
                    <li>
                        <a href="#" class="link">
                            <img src="@/assets/images/icons/adventurer.svg" alt="Advanture" class="icon"/>
                            Advanture    
                        </a>
                    </li>
                    <li>
                        <a href="#" class="link">
                            <img src="@/assets/images/icons/hiking.svg" alt="Hiking" class="icon"/>
                            Hiking
                        </a>
                    </li>
                    <li>
                        <a href="#" class="link">
                            <img src="@/assets/images/icons/fishing.svg" alt="Fishing" class="icon"/>    
                            Fishing
                        </a>
                    </li>
                    <li>
                        <a href="#" class="link">
                            <img src="@/assets/images/icons/camping.svg" alt="Camping" class="icon"/>     
                            Camping
                        </a>
                    </li>
                    <li>
                        <a href="#" class="link">
                            <img src="@/assets/images/icons/climbing.svg" alt="climping" class="icon"/>   
                            climping
                        </a>
                    </li>
                    <li>
                        <a href="#" class="link">
                            <img src="@/assets/images/icons/biking.svg" alt="biking" class="icon"/>   
                            biking
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>
<script>
import {ref} from 'vue'
export default {
    setup() {
        const sideBarIsShow = ref(false)
        return {sideBarIsShow}
    }
}
</script>
