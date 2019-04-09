<template>
  <Page>
    <ActionBar title="Welcome to NativeScript-Vue!"/>
    <StackLayout>
      <Label class="message" text="OLD SYNTAX (slot-scope)" col="0" row="0"/>
      <CurrentUser>
        <template slot-scope="scope">{{scope.user.firstName}} {{scope.user.lastName}}</template>
      </CurrentUser>

      <Label class="message" text="NEW SYNTAX (v-slot)" col="0" row="0"/>
      <CurrentUser>
        <template v-slot="scope">{{ scope ? scope.user.firstName : '(scope is not defined)'}}</template>
      </CurrentUser>
    </StackLayout>
  </Page>
</template>

<script >
import CurrentUser from "./CurrentUser";

export default {
  components: { CurrentUser },
  data() {
    return {};
  }
};
</script>

<style scoped>
ActionBar {
  background-color: #53ba82;
  color: #ffffff;
}

.message {
  vertical-align: center;
  text-align: center;
  font-size: 20;
  color: #333333;
  margin-top: 50;
}
</style>
