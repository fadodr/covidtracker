<template>
  <div class="container-fluid">
    <Header @togglebutton="buttontoggled"/>
    <Homepage :class="{'isactive' : isActive}"/>
    <Footer :class="{'isactive' : isActive}"/>
  </div>
</template>

<script>
import Homepage from './components/hompage'
import Footer from './components/footer'
import Header from './components/header'
export default {
  components : {
    Homepage,
    Footer,
    Header
  },
  data(){
    return {
      isActive : false
    }
  },
  methods: {
    buttontoggled() {
      this.isActive = !this.isActive
    }
  },
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
  @font-face {
  font-family: "Graphik";
  src: local("Graphik"),
   url(./assets/fonts/Graphikfont/GraphikRegular.otf) format("truetype");
}
.container-fluid {
  background-color: #F2F3F7;
}
.isactive {
  display: block;
}
@media screen and (max-width : 880px) {
  .isactive {
  display: none;
}
}
</style>
