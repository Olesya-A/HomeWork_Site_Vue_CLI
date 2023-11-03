<template>
  <Main />
  <Blog />
  <BlogDetails />
  <ProjectComponent />
</template>

<script>
import Main from "./components/Main.vue";
import Blog from "./components/Blog.vue";
import BlogDetails from "./components/BlogDetails.vue";
import ProjectComponent from "./components/ProjectComponent.vue";

export default {
  components: { Main, Blog, BlogDetails, ProjectComponent },
};
</script>

<style lang="scss"></style>
