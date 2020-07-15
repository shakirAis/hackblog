<template>
  <div class="header">
    <b-container fluid>
      <b-row>
        <b-col md="3">
          <div class="logo"><Logo /></div>
        </b-col>
        <b-col md="6" offset-md="3">
          <div class="nav_wrapper">
            <b-row class="text-center">
              <b-col md="3">
                <NLink to="/">Хроники Берлина</NLink>
              </b-col>
              <b-col md="3">
                <NLink to="/">О программировании</NLink>
              </b-col>
              <b-col md="3">
                <NLink to="/">О дизайне</NLink>
              </b-col>
              <b-col md="2">
                <NLink to="/">Обо мне</NLink>
              </b-col>
              <b-col md="1"></b-col>
            </b-row>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";

export default {
  components: {
    Logo
  }
};
</script>

<style>
.wrapper {
  width: 100%;
}
.header,
.footer {
  background-color: #82bdbd;
  height: 90px;
}
.nav_wrapper {
  width: 100%;
  display: inline-block;
}
.logo {
  height: 90px;
}
a {
  height: inherit;
  display: inline-block;
  line-height: 90px;
  font-size: 18px;
  font-family: "Roboto", sans-serif;
  font-weight: 500;
  color: #ffffeb;
}
a:hover {
  color: #ffffeb;
}
</style>
