<template>
  <the-header title="RememberMe"></the-header>
  <stored-resources :resources="storedResources"></stored-resources>
</template>

<script>
import StoredResources from './components/learning-resources/StoredResources.vue';
import TheHeader from './components/layouts/TheHeader.vue';

export default {
  components: {
    StoredResources,
    TheHeader,
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

<style>
@import url('https://fonts.googleapis.com/css2?family=Jost&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Jost', sans-serif;
}

body {
  margin: 0;
}
</style>
