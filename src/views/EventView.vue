<template>
    <div class="row">
        <!-- <section-title title="" /> -->
        <event-section />
    </div>
</template>

<script>
// import SectionTitle from '@/components/layout/SectionTitle.vue'
import EventSection from '@/components/event/EventSection.vue'

    export default {
        name: "EventView",
        components:{
            // SectionTitle,
            EventSection,
  
           
        }
    }
</script>

<style lang="scss" scoped>

</style>