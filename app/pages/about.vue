<template>
    <div>
        <PageBanner pageBannerHeading="About"/>
        <PersonalDetails/>
    </div>
</template>
<script setup>
import PersonalDetails from '~/components/about/PersonalDetails.vue';
import PageBanner from '~/components/PageBanner.vue';




</script>
<style scoped>
    h1 {
      color: #333;
    }
    </style>