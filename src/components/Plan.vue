<template>
    <div class="plan">
        <img :src="planData.src" :alt="planData.name"/>
        <h2>{{planData.name}}</h2>
    </div>
</template>
<script>


export default {
    props:["planData"]
}
</script>
