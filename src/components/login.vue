<template>
  <div class="container-fluid">
  <form class="form-horizontal" action="." method="post">
    <input type="hidden" name="isFirst" value="no">
    <div class="control-group">
      <label class="control-label">身分別：</label>
      <label class="checkbox inline">
        <input type="radio" name="myLevel" id="student" checked=""> 一般考生
        <input type="radio" name="myLevel" id="admin"> 監考與管理人員
        <input type="radio" name="myLevel" id="fraud"> 詐騙集團
      </label>
    </div>
    <div class="control-group">
      <label class="control-label" id="myAccount">身分證字號：</label>
      <div class="controls">
        <input type="text" id="inputID" name="id" value="">
        <span class="text-error">
        </span>
      </div>
    </div>
    <div class="control-group">
      <label class="control-label">密碼：</label>
      <div class="controls">
        <input type="password" name="pw">
      </div>
    </div>
    <div class="control-group">
      <label class="control-label">
                    <span id="new_captcha">
                        <img src="1682480151_9462.jpg" width="90" height="30" style="border:0;" alt=" ">
                    </span>
      </label>
      <div class="controls">
        <input type="text" name="captcha" placeholder="請輸入左圖出現的文字">
        <span class="text-error">
        </span>
      </div>
    </div>
    <div class="control-group">
      <div class="controls">
        <input class="btn btn-primary" type="submit" value="登入" onclick="validateForm()">
      </div>
    </div>
  </form>
  </div>
</template>

<script>
export default {
  name: "login"
}
</script>

<style scoped>

article, aside,
details, figcaption,
figure, footer,
header, hgroup,
nav, section {
  display: block;
}

audio, canvas, video {
  display: inline-block;
}

audio:not([controls]) {
  display: none;
}

html {
  font-size: 100%;
  text-size-adjust: 100%;
}

a:focus {
  outline: -webkit-focus-ring-color auto 5px;
  outline-offset: -2px;
}

a:hover, a:active {
  outline: 0px;
}

sub, sup {
  position: relative;
  font-size: 75%;
  line-height: 0;
  vertical-align: baseline;
}

sup {
  top: -0.5em;
}

sub {
  bottom: -0.25em;
}

img {
  max-width: 100%;
  height: auto;
  vertical-align: middle;
  border: 0px;
}

button, input, select, textarea {
  margin: 0px;
  font-size: 100%;
  vertical-align: middle;
}

button, input {
  line-height: normal;
}

button, html input[type="button"], input[type="reset"], input[type="submit"] {
  appearance: button;
  cursor: pointer;
}

label, select, button, input[type="button"], input[type="reset"], input[type="submit"], input[type="radio"], input[type="checkbox"] {
  cursor: pointer;
}

input[type="search"] {
  box-sizing: content-box;
  appearance: textfield;
}

input[type="search"]::-webkit-search-decoration, input[type="search"]::-webkit-search-cancel-button {
  appearance: none;
}

textarea {
  overflow: auto;
  vertical-align: top;
}

body {
  margin: 0px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 16px;
  line-height: 20px;
  color: rgb(51, 51, 51);
  background-color: rgb(199, 237, 204);
}

a {
  color: rgb(0, 136, 204);
  text-decoration: none;
}

a:hover, a:focus {
  color: rgb(0, 85, 128);
  text-decoration: underline;
}

[class*="span"] {
  float: left;
  min-height: 1px;
  margin-left: 20px;
}

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

.container-fluid::after {
  clear: both;
}

p {
  margin: 0px 0px 10px;
}

small {
  font-size: 85%;
}

strong {
  font-weight: bold;
}

em {
  font-style: italic;
}

cite {
  font-style: normal;
}

.text-error {
  color: rgb(185, 74, 72);
}

a.text-error:hover, a.text-error:focus {
  color: rgb(149, 59, 57);
}

h1, h2, h3, h4, h5, h6 {
  margin: 10px 0px;
  font-family: inherit;
  font-weight: bold;
  line-height: 20px;
  color: inherit;
  text-rendering: optimizelegibility;
}

h1 small, h2 small, h3 small, h4 small, h5 small, h6 small {
  font-weight: normal;
  line-height: 1;
  color: rgb(153, 153, 153);
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

h3 {
  font-size: 28px;
}

h4 {
  font-size: 20px;
}

h5 {
  font-size: 16px;
}

h6 {
  font-size: 13.6px;
}

h1 small {
  font-size: 28px;
}

h2 small {
  font-size: 20px;
}

h3 small {
  font-size: 16px;
}

h4 small {
  font-size: 16px;
}

ul, ol {
  padding: 0px;
  margin: 0px 0px 10px 25px;
}

ul ul, ul ol, ol ol, ol ul {
  margin-bottom: 0px;
}

li {
  line-height: 20px;
}

ul.inline, ol.inline {
  margin-left: 0px;
  list-style: none;
}

ul.inline > li, ol.inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}

dl {
  margin-bottom: 20px;
}

dt, dd {
  line-height: 20px;
}

dt {
  font-weight: bold;
}

dd {
  margin-left: 10px;
}

hr {
  margin: 20px 0px;
  border-width: 1px 0px;
  border-right-style: initial;
  border-left-style: initial;
  border-right-color: initial;
  border-left-color: initial;
  border-image: initial;
  border-top-style: solid;
  border-top-color: rgb(238, 238, 238);
  border-bottom-style: solid;
  border-bottom-color: rgb(255, 255, 255);
}

abbr[title], abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted rgb(153, 153, 153);
}

blockquote {
  padding: 0px 0px 0px 15px;
  margin: 0px 0px 20px;
  border-left: 5px solid rgb(238, 238, 238);
}

blockquote p {
  margin-bottom: 0px;
  font-size: 20px;
  font-weight: 300;
  line-height: 1.25;
}

blockquote small {
  display: block;
  line-height: 20px;
  color: rgb(153, 153, 153);
}

blockquote small::before {
  content: "— ";
}

q::before, q::after, blockquote::before, blockquote::after {
  content: "";
}

address {
  display: block;
  margin-bottom: 20px;
  font-style: normal;
  line-height: 20px;
}

code, pre {
  padding: 0px 3px 2px;
  font-family: Monaco, Menlo, Consolas, "Courier New", monospace;
  font-size: 14px;
  color: rgb(51, 51, 51);
  border-radius: 3px;
}

code {
  padding: 2px 4px;
  color: rgb(221, 17, 68);
  background-color: rgb(247, 247, 249);
  border: 1px solid rgb(225, 225, 232);
  white-space: nowrap;
}

pre {
  display: block;
  padding: 9.5px;
  margin: 0px 0px 10px;
  font-size: 15px;
  line-height: 20px;
  word-break: break-all;
  overflow-wrap: break-word;
  white-space: pre-wrap;
  background-color: rgb(245, 245, 245);
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 4px;
}

pre code {
  padding: 0px;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border: 0px;
}

.btn .label, .btn .badge {
  position: relative;
  top: -1px;
}

table {
  max-width: 100%;
  background-color: rgb(255, 255, 255);
  border-collapse: collapse;
  border-spacing: 0px;
}

form {
  margin: 0px 0px 20px;
}

fieldset {
  padding: 0px;
  margin: 0px;
  border: 0px;
}

legend {
  display: flex;
  width: 100%;
  padding: 0px;
  margin-bottom: 20px;
  font-size: 24px;
  line-height: 40px;
  color: rgb(51, 51, 51);
  border-width: 0px 0px 1px;
  border-top-style: initial;
  border-right-style: initial;
  border-left-style: initial;
  border-top-color: initial;
  border-right-color: initial;
  border-left-color: initial;
  border-image: initial;
  border-bottom-style: solid;
  border-bottom-color: rgb(229, 229, 229);
}

legend small {
  font-size: 15px;
  color: rgb(153, 153, 153);
}

label, input, button, select, textarea {
  font-size: 16px;
  font-weight: normal;
  line-height: 20px;
}

input, button, select, textarea {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}

label {
  display: flex;
  margin-bottom: 5px;
}

textarea {
  height: auto;
}

input[type="radio"], input[type="checkbox"] {
  margin: 4px 0px 0px;
  line-height: normal;
}

input[type="file"], input[type="image"], input[type="submit"], input[type="reset"], input[type="button"], input[type="radio"], input[type="checkbox"] {
  width: auto;
}

select, input[type="file"] {
  height: 30px;
  line-height: 30px;
}

select {
  width: 220px;
  border: 1px solid rgb(204, 204, 204);
  background-color: rgb(255, 255, 255);
}

select[multiple], select[size] {
  height: auto;
}

select:focus, input[type="file"]:focus, input[type="radio"]:focus, input[type="checkbox"]:focus {
  outline: -webkit-focus-ring-color auto 5px;
  outline-offset: -2px;
}

input::-webkit-input-placeholder, textarea::-webkit-input-placeholder {
  color: rgb(153, 153, 153);
}

.radio, .checkbox {
  min-height: 20px;
  padding-left: 20px;
}

.radio input[type="radio"], .checkbox input[type="checkbox"] {
  float: left;
  margin-left: -20px;
}

.controls > .radio:first-child, .controls > .checkbox:first-child {
  padding-top: 5px;
}

.radio.inline, .checkbox.inline {
  display: inline-block;
  padding-top: 5px;
  margin-bottom: 0px;
  vertical-align: middle;
}

.radio.inline + .radio.inline, .checkbox.inline + .checkbox.inline {
  margin-left: 10px;
}

input[disabled], select[disabled], textarea[disabled], input[readonly], select[readonly], textarea[readonly] {
  cursor: not-allowed;
  background-color: rgb(238, 238, 238);
}

input[type="radio"][disabled], input[type="checkbox"][disabled], input[type="radio"][readonly], input[type="checkbox"][readonly] {
  background-color: transparent;
}

.control-group.warning .control-label, .control-group.warning .help-block, .control-group.warning .help-inline {
  color: rgb(192, 152, 83);
}

.control-group.warning .checkbox, .control-group.warning .radio, .control-group.warning input, .control-group.warning select, .control-group.warning textarea {
  color: rgb(192, 152, 83);
}

.control-group.error .control-label, .control-group.error .help-block, .control-group.error .help-inline {
  color: rgb(185, 74, 72);
}

.control-group.error .checkbox, .control-group.error .radio, .control-group.error input, .control-group.error select, .control-group.error textarea {
  color: rgb(185, 74, 72);
}

.control-group.success .control-label, .control-group.success .help-block, .control-group.success .help-inline {
  color: rgb(70, 136, 71);
}

.control-group.success .checkbox, .control-group.success .radio, .control-group.success input, .control-group.success select, .control-group.success textarea {
  color: rgb(70, 136, 71);
}

.control-group.info .control-label, .control-group.info .help-block, .control-group.info .help-inline {
  color: rgb(58, 135, 173);
}

.control-group.info .checkbox, .control-group.info .radio, .control-group.info input, .control-group.info select, .control-group.info textarea {
  color: rgb(58, 135, 173);
}

input:focus:invalid, textarea:focus:invalid, select:focus:invalid {
  color: rgb(185, 74, 72);
  border-color: rgb(238, 95, 91);
}

input:focus:invalid:focus, textarea:focus:invalid:focus, select:focus:invalid:focus {
  border-color: rgb(233, 50, 45);
  box-shadow: rgb(248, 185, 183) 0px 0px 6px;
}

.input-append .add-on, .input-prepend .add-on, .input-append .btn, .input-prepend .btn, .input-append .btn-group > .dropdown-toggle, .input-prepend .btn-group > .dropdown-toggle {
  vertical-align: top;
  border-radius: 0px;
}

.input-prepend .add-on, .input-prepend .btn {
  margin-right: -1px;
}

.input-prepend .add-on:first-child, .input-prepend .btn:first-child {
  border-radius: 4px 0px 0px 4px;
}

.input-append input + .btn-group .btn:last-child, .input-append select + .btn-group .btn:last-child, .input-append .uneditable-input + .btn-group .btn:last-child {
  border-radius: 0px 4px 4px 0px;
}

.input-append .add-on, .input-append .btn, .input-append .btn-group {
  margin-left: -1px;
}

.input-append .add-on:last-child, .input-append .btn:last-child, .input-append .btn-group:last-child > .dropdown-toggle {
  border-radius: 0px 4px 4px 0px;
}

.input-prepend.input-append input + .btn-group .btn, .input-prepend.input-append select + .btn-group .btn, .input-prepend.input-append .uneditable-input + .btn-group .btn {
  border-radius: 0px 4px 4px 0px;
}

.input-prepend.input-append .add-on:first-child, .input-prepend.input-append .btn:first-child {
  margin-right: -1px;
  border-radius: 4px 0px 0px 4px;
}

.input-prepend.input-append .add-on:last-child, .input-prepend.input-append .btn:last-child {
  margin-left: -1px;
  border-radius: 0px 4px 4px 0px;
}

.form-search .input-append .btn {
  border-radius: 0px 14px 14px 0px;
}

.form-search .input-prepend .btn {
  border-radius: 14px 0px 0px 14px;
}

.form-search input, .form-inline input, .form-horizontal input, .form-search textarea, .form-inline textarea, .form-horizontal textarea, .form-search select, .form-inline select, .form-horizontal select, .form-search .help-inline, .form-inline .help-inline, .form-horizontal .help-inline, .form-search .uneditable-input, .form-inline .uneditable-input, .form-horizontal .uneditable-input, .form-search .input-prepend, .form-inline .input-prepend, .form-horizontal .input-prepend, .form-search .input-append, .form-inline .input-append, .form-horizontal .input-append {
  display: inline-block;
  margin-bottom: 0px;
  vertical-align: middle;
}

.form-search .hide, .form-inline .hide, .form-horizontal .hide {
  display: none;
}

.form-search .radio, .form-search .checkbox, .form-inline .radio, .form-inline .checkbox {
  padding-left: 0px;
  margin-bottom: 0px;
  vertical-align: middle;
}

.form-search .radio input[type="radio"], .form-search .checkbox input[type="checkbox"], .form-inline .radio input[type="radio"], .form-inline .checkbox input[type="checkbox"] {
  float: left;
  margin-right: 3px;
  margin-left: 0px;
}

.control-group {
  margin-bottom: 10px;
}

legend + .control-group {
  margin-top: 20px;
}

.form-horizontal .control-group {
  margin-bottom: 20px;
}

.form-horizontal .control-group::before, .form-horizontal .control-group::after {
  display: table;
  content: "";
  line-height: 0;
}

.form-horizontal .control-group::after {
  clear: both;
}

.form-horizontal .control-label {
  float: left;
  width: 160px;
  padding-top: 5px;
  text-align: right;
}

.form-horizontal .controls {
  margin-left: 180px;
}

.form-horizontal .controls:first-child {
}

.form-horizontal .help-block {
  margin-bottom: 0px;
}

.form-horizontal input + .help-block, .form-horizontal select + .help-block, .form-horizontal textarea + .help-block, .form-horizontal .uneditable-input + .help-block, .form-horizontal .input-prepend + .help-block, .form-horizontal .input-append + .help-block {
  margin-top: 10px;
}

.form-horizontal .form-actions {
  padding-left: 180px;
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

.btn:active, .btn.active {
}

.btn:first-child {
}

.btn:hover, .btn:focus {
  color: rgb(51, 51, 51);
  text-decoration: none;
  background-position: 0px -15px;
  transition: background-position 0.1s linear 0s;
}

.btn:focus {
  outline: -webkit-focus-ring-color auto 5px;
  outline-offset: -2px;
}

.btn.active, .btn:active {
  background-image: none;
  outline: 0px;
  box-shadow: rgba(0, 0, 0, 0.15) 0px 2px 4px inset, rgba(0, 0, 0, 0.05) 0px 1px 2px;
}

.btn-primary {
  color: rgb(255, 255, 255);
  text-shadow: rgba(0, 0, 0, 0.25) 0px -1px 0px;
  background-color: rgb(0, 109, 204);
  background-image: linear-gradient(rgb(0, 136, 204), rgb(0, 68, 204));
  background-repeat: repeat-x;
  border-color: rgba(0, 0, 0, 0.1) rgba(0, 0, 0, 0.1) rgba(0, 0, 0, 0.25);
}

.btn-primary:hover, .btn-primary:focus, .btn-primary:active, .btn-primary.active, .btn-primary.disabled, .btn-primary[disabled] {
  color: rgb(255, 255, 255);
  background-color: rgb(0, 68, 204);
}

.btn-primary:active, .btn-primary.active {
}

button.btn, input[type="submit"].btn {
}

[class^="icon-"], [class*=" icon-"] {
  display: inline-block;
  width: 14px;
  height: 14px;
  line-height: 14px;
  vertical-align: text-top;
  background-image: url("../img/glyphicons-halflings.png");
  background-position: 14px 14px;
  background-repeat: no-repeat;
  margin-top: 1px;
}

.icon-refresh {
  background-position: -240px -24px;
}

.btn-toolbar > .btn + .btn, .btn-toolbar > .btn-group + .btn, .btn-toolbar > .btn + .btn-group {
  margin-left: 5px;
}

.btn-group > .btn {
  position: relative;
  border-radius: 0px;
}

.btn-group > .btn + .btn {
  margin-left: -1px;
}

.btn-group > .btn, .btn-group > .dropdown-menu, .btn-group > .popover {
  font-size: 16px;
}

.btn-group > .btn:first-child {
  margin-left: 0px;
  border-top-left-radius: 4px;
  border-bottom-left-radius: 4px;
}

.btn-group > .btn:last-child, .btn-group > .dropdown-toggle {
  border-top-right-radius: 4px;
  border-bottom-right-radius: 4px;
}

.btn-group > .btn:hover, .btn-group > .btn:focus, .btn-group > .btn:active, .btn-group > .btn.active {
  z-index: 2;
}

.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
  box-shadow: rgba(255, 255, 255, 0.125) 1px 0px 0px inset, rgba(255, 255, 255, 0.2) 0px 1px 0px inset, rgba(0, 0, 0, 0.05) 0px 1px 2px;
}

.btn .caret {
  margin-top: 8px;
  margin-left: 0px;
}

.btn-primary .caret, .btn-warning .caret, .btn-danger .caret, .btn-info .caret, .btn-success .caret, .btn-inverse .caret {
  border-top-color: rgb(255, 255, 255);
  border-bottom-color: rgb(255, 255, 255);
}

.btn-group-vertical > .btn {
  display: block;
  float: none;
  max-width: 100%;
  border-radius: 0px;
}

.btn-group-vertical > .btn + .btn {
  margin-left: 0px;
  margin-top: -1px;
}

.btn-group-vertical > .btn:first-child {
  border-radius: 4px 4px 0px 0px;
}

.btn-group-vertical > .btn:last-child {
  border-radius: 0px 0px 4px 4px;
}

.navbar .btn, .navbar .btn-group {
  margin-top: 5px;
}

.navbar .btn-group .btn, .navbar .input-prepend .btn, .navbar .input-append .btn, .navbar .input-prepend .btn-group, .navbar .input-append .btn-group {
  margin-top: 0px;
}

.navbar-form input, .navbar-form select, .navbar-form .radio, .navbar-form .checkbox {
  margin-top: 5px;
}

.navbar-form input, .navbar-form select, .navbar-form .btn {
  display: inline-block;
  margin-bottom: 0px;
}

.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0px;
}

.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}


</style>