<template>
  <Main />
  <Blog />
  <BlogDetails />
  <ProjectComponent />
  <ProjectDetailsComponent />
</template>

<script>
import Main from "./components/Main.vue";
import Blog from "./components/Blog.vue";
import BlogDetails from "./components/BlogDetails.vue";
import ProjectComponent from "./components/ProjectComponent.vue";
import ProjectDetailsComponent from "./components/ProjectDetailsComponent.vue";

export default {
  components: {
    Main,
    Blog,
    BlogDetails,
    ProjectComponent,
    ProjectDetailsComponent,
  },
};
</script>

<style lang="scss"></style>
