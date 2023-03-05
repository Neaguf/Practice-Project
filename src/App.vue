<template>
  <stored-resources :resources="storedResources"></stored-resources>
</template>

<script>
import storedResources from './components/learning-resource/StoredResource.vue';
export default {
  components: {
    storedResources,
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

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>