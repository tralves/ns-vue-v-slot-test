<template>
  <Label>
    <slot :user="user">{{ user.firstName }}</slot>
  </Label>
</template>

<script>
export default {
  data() {
    return {
      user: {
        firstName: "Tiago",
        lastName: "Alves"
      }
    };
  }
};
</script>

<style>
</style>
