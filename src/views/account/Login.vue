<template>
  <div class="account">
    <div class="form-wrap">
      <a-form name="custom-validation" ref="ruleForm">
        <a-form-item>
          <label>用户名</label>
          <a-input type="text" autocomplete="off" />
        </a-form-item>

        <a-form-item>
          <label>密码</label>
          <a-input type="password" autocomplete="off" />
        </a-form-item>

        <a-form-item>
          <div id="captcha-dom" class="nc-container"></div>
          <!--No-Captcha渲染的位置，其中 class 中必须包含 nc-container-->
        </a-form-item>
        <!-- <a-form-item> -->
        <!-- <Captcha /> -->
        <!-- <-Captcha></Captcha> -->
        <!-- </a-form-item> -->

        <a-form-item>
          <a-button type="primary" html-type="submit" block>
            登录
          </a-button>
        </a-form-item>
      </a-form>
      <div class="text-center fs-12">
        <router-link to="/forget" class="color-white">忘记密码</router-link> |
        <router-link to="/register" class="color-white">注册</router-link>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref, reactive } from "vue";

export default defineComponent({
  name: "Home",
  components: {},
  setup(props) {
    const count = ref<number>(10);
    console.log(count.value);
  },
});
</script>
<style lang="scss">
@import "./style.scss";
</style>
