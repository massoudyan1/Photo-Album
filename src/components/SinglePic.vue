<template>
    <img 
        class="cell" 
        :id="pic.id" 
        :src="require(`../../assets/${pic.url}.jpg`)" 
        :alt="pic.title">

    <div 
        id="more"
        v-if="showDetails">
        <img 
            :src="require(`../../assets/${pic.url}.jpg`)"  
            alt="" id="showing">

        <div id="showing">
            <h3> {{pic.title}} </h3>
        </div>
    </div>

</template>

<script>
export default {
    props: ['pic']
}
</script>

<style>

</style>