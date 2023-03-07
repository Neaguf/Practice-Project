<template>
  <base-card>
    <base-button
      @click="setSelectedTab('stored-resource')"
      :mode="storedResButtonMode"
      >Stored Resources
    </base-button>
    <base-button
      @click="setSelectedTab('add-resource')"
      :mode="addResButtonMode"
    >
      Add Resource</base-button
    >
  </base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import StoredResource from './StoredResource.vue';
import AddResource from './AddResource.vue';
export default {
  components: {
    StoredResource,
    AddResource,
  },
  data() {
    return {
      selectedTab: 'stored-resources',
      storedResources: [
        {
          id: 'official-guild',
          title: 'Official guild',
          description: 'The official vue js documentation,',
          link: 'https://vuejs.org/v2/guide/',
        },
        {
          id: 'Google',
          title: 'Google',
          description: 'The official vue js documentation,',
          link: 'https://vuejs.org/v2/guide/',
        },
      ],
    };
  },
  provide() {
    return {
      resources: this.storedResources,
    };
  },
  computed: {
    storedResButtonMode() {
      return this.selectedTab === 'stored-resources' ? null : 'flat';
    },
    addResButtonMode() {
      return this.selectedTab === 'add-resource' ? null : 'flat';
    },
  },

  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },
  },
};
</script>
