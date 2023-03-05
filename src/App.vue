<template>
  <ul>
    <learning-resource
      v-for="res in storedResources"
      :key="res.key"
      :title="res.title"
      :description="res.description"
      :link="res.link"
    ></learning-resource>
  </ul>
</template>

<script>
import LearningResource from './components/learning-resource/LearningResource.vue';
export default {
  components: {
    LearningResource,
  },
  data() {
    return {
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
};
</script>

<style></style>