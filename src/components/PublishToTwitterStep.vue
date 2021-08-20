<template>
  <PublishToSocialStep>
    <form @submit.prevent="submit">
      <div>
        <p><b>enter your tweet:</b></p>
        <input v-model="text" type="text"/>
      </div>
      <div>
        <p><b>tweet preview:</b></p>
        <p>{{ text }}</p>
      </div>
      <button>Submit</button>
    </form>
  </PublishToSocialStep>
</template>

<script>
import PublishToSocialStep from "./PublishToSocialStep.vue";

export default {
  components: {PublishToSocialStep},
  data() {
    return {
      text: 'initial',
    }
  },
  methods: {
    submit() {
      alert(this.text);
    },
  },
};
</script>
