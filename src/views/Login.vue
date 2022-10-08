<template>
  <div class="login-container">
    <img src="@/assets/loginBackground.png" alt="" class="login-background" />
    <img src="@/assets/name.png" alt="" class="name" />
    <LoginBox v-if="isRegister" @register="goRegister"></LoginBox>
    <RegisterBox v-else @suc-register="backLogin"></RegisterBox>
  </div>
</template>

<script>
import LoginBox from '@/components/login/LoginBox.vue'
import RegisterBox from '@/components/login/RegisterBox.vue'
export default {
  name: 'FarmCusLogin',
  components: { LoginBox, RegisterBox },
  data() {
    return {
      isRegister: true
    }
  },
  methods: {
    goRegister(val) {
      this.isRegister = val
    },
    backLogin(val) {
      this.isRegister = val
    }
  }
}
</script>
<style lang="less" scoped>
.login-background {
  z-index: -1;
  position: absolute;
  scale: 2;
}
.name {
  display: block;
  margin: 0 auto;
}
</style>
