<template>
  <appheader></appheader>
  <el-container class="backgroundDiv" :style="backgroundDiv">
    <el-main > Main
    </el-main>
    <el-aside width="45%" class="backgroundDiv2" :style="backgroundDiv2">
<el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="100px" class="demo-ruleForm">
  <el-form-item label="ユーザー名" prop="user">
    <el-input v-model="ruleForm.user" placeholder="ユーザー名を入力してください"></el-input>
  </el-form-item>
 <el-form-item label="パスワード" prop="pass">
    <el-input type="password" v-model="ruleForm.pass" placeholder="パスワードを入力してください" autocomplete="on"></el-input>
  </el-form-item>
  <el-form-item>
    <el-button type="primary" @click="submitForm('ruleForm')">ログイン</el-button>
    <el-button type="primary" @click="$router.push('/')">戻る</el-button>
  </el-form-item>
</el-form>
    </el-aside>
  </el-container>
  <appfooter></appfooter>
</template>
<script>
import appfooter from '@/components/Footer.vue'
import appheader from '@/components/Header.vue'
export default {
  data() {
      return {
      backgroundDiv: {
        backgroundImage: 'url(' + require('../assets/background/login_background3.jpg') + ')',
        backgroundRepeat: 'no-repeat',
        backgroundSize: '100% 100%'

      },
      backgroundDiv2: {
        backgroundImage: 'url(' + require('../assets/background/login_background4.jpg') + ')',
        backgroundRepeat: 'no-repeat',
        backgroundSize: '100% 350px'
      },
        ruleForm: {
          user: '',
          pass: ''
        },
        rules: {
          user: [
            { required: true, message: 'ユーザー名を入力してください', trigger: 'blur' },
            { min: 8, max: 16, message: '8~16桁の英数字を入力してください', trigger: 'blur' }
          ],
          pass: [
            { required: true, message: 'パスワードを入力してください', trigger: 'blur' },
              { min: 8, max: 16, message: '8~16桁の英数字を入力してください', trigger: 'blur' }
          ]
        }
      };
    },
    methods: {
      submitForm(formName) {
        this.$refs[formName].validate((valid) => {
          if (valid) {
            alert('submit!');
          } else {
            console.log('error submit!!');
            return false;
          }
        });
      }
    },
   components: {
    appfooter,
    appheader
  }
  }
</script>
<style scoped>
 .el-aside {
   background-color: transparent;
    text-align: center;
    line-height: 480px;
  }

  .el-main {
    background-color: transparent;
    text-align: center;
    line-height: 480px;
  }
</style>

