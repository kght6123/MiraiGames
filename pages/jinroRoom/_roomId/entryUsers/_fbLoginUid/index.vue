<template>
  <div>
    RoomId : {{ $route.params.roomId }}<br />
    LoginUid : {{ $route.params.fbLoginUid }}<br />
    他の参加者を待っています。しばらく、お待ちください。。。<br />
    <atom-loading-animation />
    <organism-waiting-member
      :roomId="$route.params.roomId"
      :fbLoginUid="$route.params.fbLoginUid"
    />
    <organism-sign-in-and-out />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      roomId: this.$route.params.roomId,
      fbLoginUid: this.$route.params.fbLoginUid,
    }
  },
})
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
</style>
