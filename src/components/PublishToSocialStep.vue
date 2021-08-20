<template>
  <AuthUserProvider v-slot="{ user }">
    <StepContainer>
      <template #content>
        <div>
          <div>
            <h1>You're logged in as {{ user.first }} {{ user.last }}!</h1>
          </div>
          <h4>Fill & submit the form below:</h4>
          <div style="border: 1px darkgray solid; padding: 5px;">
            <slot/>
          </div>
        </div>
      </template>
    </StepContainer>
  </AuthUserProvider>
</template>

<script>
import StepContainer from "./StepContainer.vue";
import AuthUserProvider from "./AuthUserProvider.vue";

export default {
  components: {
    AuthUserProvider,
    StepContainer,
  },
};
</script>
