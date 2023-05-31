<template>
  <div class="container-fluid">
    <a id="forgetPW" class="btn" href="https://cpe.cse.nsysu.edu.tw/cpe/forget_password">忘記密碼</a>
    <a id="addNewAccount" class="btn" href="https://cpe.cse.nsysu.edu.tw/cpe/new_account">申請新帳號</a>

  </div>
</template>

<script>
export default {
  name: "direct"
}
</script>

<style scoped>
.container-fluid {
  padding-right: 20px;
  padding-left: 20px;
  margin: 0px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 16px;
  line-height: 20px;
  color: rgb(51, 51, 51);
  background-color: rgb(199, 237, 204);
}

.container-fluid::before, .container-fluid::after {
  display: table;
  content: "";
  line-height: 0;
}
.btn {
  display: inline-block;
  padding: 4px 12px;
  margin-bottom: 0px;
  font-size: 16px;
  line-height: 20px;
  text-align: center;
  vertical-align: middle;
  cursor: pointer;
  color: rgb(51, 51, 51);
  text-shadow: rgba(255, 255, 255, 0.75) 0px 1px 1px;
  background-color: rgb(245, 245, 245);
  background-image: linear-gradient(rgb(255, 255, 255), rgb(230, 230, 230));
  background-repeat: repeat-x;
  border-width: 1px;
  border-style: solid;
  border-color: rgb(204, 204, 204) rgb(204, 204, 204) rgb(179, 179, 179);
  border-image: initial;
  border-radius: 4px;
  box-shadow: rgba(255, 255, 255, 0.2) 0px 1px 0px inset, rgba(0, 0, 0, 0.05) 0px 1px 2px;
}

.btn:hover, .btn:focus, .btn:active, .btn.active, .btn.disabled, .btn[disabled] {
  color: rgb(51, 51, 51);
  background-color: rgb(230, 230, 230);
}
a {
  color: rgb(0, 136, 204);
  text-decoration: none;
}

a:hover, a:focus {
  color: rgb(0, 85, 128);
  text-decoration: underline;
}
</style>