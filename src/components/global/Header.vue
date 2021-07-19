<template>
  <header :class="{'pricing-animate':isPricing}">
      <Nav/>
    <div class="gate-container"></div>
    <div class="main-hero" >
      <div class="hero-content">
        <div class="hero-welcome">
            <h1 class="title">travel</h1>
            <p class="description">Travel and visit the national parks, enjoy your life.</p>
            <div class="d-flex">
                <button class="explore-button ml-auto explore" @click="isPricing = !isPricing">Explore</button>
            </div>
        </div>

        <div class="pricing">
            <h2 class="title">
                <!-- National Parks -->
                National
                Parks
            </h2>
            <div class="d-flex plans-container">
                <Plan @click="isPricing = false" v-for="plan in plans" :key="plan.id" :planData="plan"/>
            </div>
        </div>
       
      </div>
    </div>
  </header>
</template>
<script>
import { ref } from 'vue'
import Plan from '@/components/Plan'
import Nav from '@/components/global/NabBar'
export default {
    components:{
        Plan:Plan,
        Nav:Nav
    },
    setup() {
        const plans = ref([
            {
                name:'arctic gates',
                id:1,
                src:require('@/assets/images/pricing/gates-arctic.jpg'),
            },
            {
                name:'Kings Canyon',
                id:2,
                src:require('@/assets/images/pricing/kings-canyon.jpg'),
            },
            {
                name:'Redwoods',
                src:require('@/assets/images/pricing/redwoods.jpg'),
                id:3,
            }
        ])
        const isPricing = ref(false);


        return {isPricing, plans}
    },
}
</script>
