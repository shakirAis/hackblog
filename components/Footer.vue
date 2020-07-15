<template>
  <div class="footer">
    <b-container fluid class="mb-0">
      <b-row class="mb-0">
        <b-col md="2" class="mb-0">
          <div class="footer_logo"><Logo /></div>
        </b-col>
        <b-col md="9" class="mb-0">
          <div class="nav_wrapper">
            <b-row class="text-center">
              <b-col md="2"></b-col>
              <b-col md="2">
                <NLink to="/">Хроники Берлина</NLink>
              </b-col>
              <b-col md="2">
                <NLink to="/">О программировании</NLink>
              </b-col>
              <b-col md="2">
                <NLink to="/">О дизайне</NLink>
              </b-col>
              <b-col md="2">
                <NLink to="/">Обо мне</NLink>
              </b-col>
              <b-col md="2"></b-col>
            </b-row>
          </div>
        </b-col>
        <b-col md="1" class="mb-0">
          <a class="telegram original_chan">tt_de</a>
          <a class="instagram original_chan">tt_de</a>
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
.footer {
  background-color: #82bdbd;
  height: 90px;
  bottom: 0;
  left: 0;
  width: 100%;
}
.nav_wrapper {
  width: 100%;
  display: inline-block;
}
.footer_logo #header_logo {
  height: 90px;
  width: 280px !important;
}
.footer_logo {
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
.telegram {
  background-image: url("../assets/telegram 1.png");
}
.instagram {
  background-image: url("../assets/instagram 1.png");
}
a.original_chan {
  background-repeat: no-repeat;
  width: 150px;
  height: 45px;
  background-size: 30px 30px;
  background-position: 0 50%;
  float: right;
  display: inline-block;
  text-align: center;
  line-height: 45px;
}
.footer a {
  font-size: 16px;
}
</style>
