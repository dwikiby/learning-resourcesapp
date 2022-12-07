<template>
  <ul>
    <learning-resource
      v-for="res in storedResources"
      :key="res.id"
      :title="res.title"
      :description="res.description"
      :link="res.link"
    ></learning-resource>
  </ul>
</template>

<script>
import LearningResource from './components/learning-resources/LearningResource.vue';

export default {
  components: {
    LearningResource,
  },
  data() {
    // data dummy store
    return {
      storedResources: [
        {
          id: 'official-guide',
          title: 'Official Guide',
          description: 'The official Vue.js documentasion.',
          link: 'https://vuejs.org',
        },
        {
          id: 'google',
          title: 'Google',
          description: 'Learn more in google...',
          link: 'https://google.org',
        },
      ],
    };
  },
};
</script>
