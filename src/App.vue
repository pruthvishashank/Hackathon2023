<template>
  <div>
    <h1>Organizational Tree</h1>
    <TreeStructure :data="treeData" />
  </div>
</template>

<script>
import TreeStructure from "./components/TreeStructure.vue";

export default {
  name: "App",
  components: {
    TreeStructure
  },
  data() {
    return {
      treeData: [
        {
          id: "parent",
          label: "Parent",
          children: [
            { id: "a", label: "Child A", children: [] },
            { id: "b", label: "Child B", children: [] },
            { id: "c", label: "Child C", children: [] }
          ]
        }
      ]
    };
  }
};
</script>