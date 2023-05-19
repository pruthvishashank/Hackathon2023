<template>
  <div>
    <ul>
      <li v-for="item in treeData" :key="item.id">
        {{ item.label }}
        <TreeStructure :data="item.children" v-if="item.children && item.children.length > 0" />
      </li>
    </ul>
  </div>
</template>


<script>
export default {
  name: "TreeStructure",
  props: {
    data: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      treeData: []
    };
  },
  mounted() {
    this.treeData = this.data;
  }
};
</script>