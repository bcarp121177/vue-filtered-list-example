<template>
  <div>
    <input type="text" v-model="search">
    <ul v-for="project in filteredProjects" :key="project.id">
      <li>{{project.name}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: ``
    };
  },
  props: {
    projects: Array
  },
  computed: {
    filteredProjects: function() {
      return this.projects.filter(project => {
        return project.name.match(this.search) !== null;
      });
    }
  }
};
</script>

<style></style>
