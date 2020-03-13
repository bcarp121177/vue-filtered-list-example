<template>
  <div>
    <div>
      <data-list endpoint="projects">
        <div slot-scope="{ data: projects }">
          <project-list :projects="projects"></project-list>
        </div>
      </data-list>
    </div>
    <sidebar>
      <component v-bind:is="componentToLoad">
        <p>help</p>
      </component>
    </sidebar>
  </div>
</template>

<script>
import DataList from "./components/DataList";
import ProjectList from "./components/ProjectList";

export default {
  name: `Project`,
  components: {
    DataList,
    ProjectList
  }
};
</script>
<style></style>
