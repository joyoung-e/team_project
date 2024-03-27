<template>
    <main>
        <selection />
       <home-search />
    </main>
</template>

<script>
    import Selection from "@/components/section/selection.vue";
    import HomeSearch from "@/components/section/HomeSearch.vue"
    export default {
        name: "HomeView",
        components: {
            Selection,
            HomeSearch,
            
        } 
    }
</script>

<style lang="scss" scoped>

</style>