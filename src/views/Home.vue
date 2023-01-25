<template>
  <div class="home">
    <HeroSection/>
    <Feed/>
  </div>
</template>

<script>
import HeroSection from "@/components/HeroSection.vue";
import Feed from "@/components/Feed.vue";

export default {
  name: "Home",
  components: {
    HeroSection,
    Feed
  }
};
</script>
