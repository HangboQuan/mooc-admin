<template>
    <div class="login-container">
        <el-form class="login-form">
            <div class="title-container">
                <h3 class="title">用户登录</h3>

            </div>

            <!-- username -->
            <el-form-item>
                <span class="svg-container">
                    <el-icon>
                        <avatar />

                    </el-icon>
                </span>
                <el-input placeholder="username" name="username" type="text"></el-input>
            </el-form-item>

            <!-- password -->
            <el-form-item>
                <span class="svg-container">
                    <el-icon>
                        <avatar />

                    </el-icon>
                </span>
                <el-input placeholder="password" name="password"></el-input>
                <span class="show-pwd">
                   <el-icon><View /></el-icon>
                </span>
            </el-form-item>

            <!-- 登录按钮 -->
            <el-button type="primary" style="width: 100%; margin-bottom: 30px;">登录</el-button>
        </el-form>
    </div>
</template>

<script setup>
    import {} from 'vue'
    import { Avatar } from '@element-plus/icons'
</script>

<style lang="scss" scoped>
$bg: #2d3a4b;
$dark_gray: #889aa4;
$light_gray: #eee;
$cursor: #fff;
.login-container {
  min-height: 100%;
  width: 100%;
  background-color: $bg;
  overflow: hidden;
  .login-form {
    position: relative;
    width: 520px;
    max-width: 100%;
    padding: 160px 35px 0;
    margin: 0 auto;
    overflow: hidden;
    :deep .el-form-item {
      border: 1px solid rgba(255, 255, 255, 0.1);
      background: rgba(0, 0, 0, 0.1);
      border-radius: 5px;
      color: #454545;
    }
    :deep .el-input {
      display: inline-block;
      height: 47px;
      width: 85%;
      --el-input-focus-border-color: none;
      --el-input-border-color: none;
      --el-input-hover-border-color: none;
      input {
        background: transparent;
        border: 0px;
        border-radius: 0px;
        padding: 12px 5px 12px 15px;
        color: red;
        height: 47px;
        caret-color: $cursor;
      }
    }
  }
  .tips {
    font-size: 16px;
    color: white;
    line-height: 24px;
  }
  .svg-container {
    padding: 6px 5px 6px 15px;
    color: $dark_gray;
    vertical-align: middle;
    display: inline-block;
  }
  .title-container {
    position: relative;
    .title {
      font-size: 26px;
      color: $light_gray;
      margin: 0px auto 40px auto;
      text-align: center;
      font-weight: bold;
    }
  }
  .show-pwd {
    position: absolute;
    right: 10px;
    font-size: 16px;
    color: $dark_gray;
    cursor: pointer;
    user-select: none;
  }
  :deep .lang-select {
    position: absolute;
    top: 10px;
    right: 0;
    background-color: #eee;
    font-size: 22px;
    padding: 4px;
    border-radius: 4px;
    cursor: pointer;
  }
}
</style>