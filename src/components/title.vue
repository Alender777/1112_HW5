<template>
  <div class="container-fluid">
    <h1>大學程式能力檢定</h1>
    <h2>Collegiate Programming Examination (CPE)</h2><br>
  </div>
</template>

<script>
export default {
  name: "titleA"
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
h1, h2, h3, h4, h5, h6 {
margin: 10px 0px;
font-family: inherit;
font-weight: bold;
line-height: 20px;
color: inherit;
text-rendering: optimizelegibility;
}
h1, h2, h3 {
line-height: 40px;
}

h1 {
font-size: 44px;
}
h2 {
font-size: 36px;
}


</style>