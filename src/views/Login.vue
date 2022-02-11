<template>
  <div class="login">
    <!-- <div class="avatar">
      <n-avatar
        round
        :size="48"
      >
        <n-icon>
          <PersonCircle />
        </n-icon>
      </n-avatar>
    </div> -->
    <n-input-group>
      <n-input size="large"
        type="password"
        show-password-on="mousedown"
        placeholder="请输入访问密码"
        :maxlength="8" >
        <template #prefix>
          <n-icon :component="LockClosedOutline" />
        </template>
      </n-input>
      <n-button type="info" size="large">
        登录
        <template #icon>
          <n-icon><LogInOutline /></n-icon>
        </template>
      </n-button>
    </n-input-group>
  </div>
</template>

<script setup>
import { 
  NInputGroup,
  NInput,
  NButton,
  NIcon,
  NAvatar
} from 'naive-ui'
import { 
  LogInOutline,
  LockClosedOutline,
  PersonCircle
} from "@vicons/ionicons5";
</script>

<style lang="scss" scoped>


.login {
  max-width: 350px;
  width: 100%;
  margin: 0 auto;
  padding: 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  .avatar {
    text-align: center;
    padding-bottom: 20px;
  }
}
</style>