<template>
  <div id="layout-default">
    <nav
      :class="{'navbar': true,'is-active': isResponsive,'is-normal': !isResponsive}"
      role="navigation"
      aria-label="main navigation">
      <div class="navbar-brand">
        <div class="avatar">
          <img
            src="/luiz.jpg"
            alt="Luiz Otávio Rodrigues">
        </div>
      </div>

      <div
        id="navbarBasicExample"
        :class="{'navbar-menu': true,'is-active': isResponsive}">
        <div class="navbar-start">
          <a
            class="navbar-item"
            href="https://www.facebook.com/luizotavior18"
            target="_blank">
            <b-icon
              icon="facebook-box"/>
          </a>
          <a
            class="navbar-item"
            href="https://github.com/luizotavior"
            target="_blank">
            <b-icon
              icon="github-circle"/>
          </a>
          <a
            class="navbar-item"
            href="https://www.linkedin.com/in/luizotavior/"
            target="_blank">
            <b-icon
              icon="linkedin"/>
          </a>
        </div>
      </div>
    </nav>
    <nuxt />
    <div id="effects">
      <div
        id="effect-left"/>
      <div
        id="effect-top"/>
    </div>
  </div>
</template>

<script>
export default {
  head () {
    return {
      script: [
        { type: 'application/ld+json', src: JSON.stringify(this.structuredData) }
      ]
    }
  },
  data() {
    return {
      isModal: false,
      isResponsive: false,
      structuredData: {
        "@context": "http://schema.org/",
        "@type": "Person",
        "name": "Luiz Otávio Rodrigues",
        "url": "https://luizotavior.com.br",
        "image": "https://luizotavior.com.br/luiz.jpg",
        "sameAs": [
          "https://www.facebook.com/luizotavior18",
          "https://github.com/luizotavior",
          "https://www.instagram.com/luiz.otavior/",
          "https://www.linkedin.com/in/luizotavior/"
        ],
        "jobTitle": "Full Stack Developer"
      },
    }
  }
}
</script>



<style lang="scss">
  @import url('https://fonts.googleapis.com/css?family=Poppins:300,400,700');
  html {
    height: 100%;
    width: 100%;
    overflow-y: auto;
  }
  body {
    min-height: 100%;
    width: 100%;
    background-color: #373841;
    overflow-y: auto;
  }
  #layout-default{
    font-family: 'Poppins', sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    overflow: hidden;
    overflow-y: auto;
    .navbar{
      margin-top: 12px;
      &.is-normal{
        background-color: transparent;
      }
      @media screen and (max-width: 1024px) {
        width: 90%;
      }
      @media screen and (min-width: 1024px) {
        background-color: transparent;
        width: 70%;
        min-width: 1024px;
      }
      &.is-active{
        @media screen and (max-width: 1024px) {
          background-color: #fff;
          position: fixed;
          top: 0px;
          left: 0px;
          width: 100%;
          margin-top: 0px;
          color: black!important;
          a.navbar-item{
            color: black;
            &:hover{
              color: black;
            }
          }
          .avatar{
            margin: 15px;
          }
        }
      }
      .avatar{
        height: 70px;
        width: 70px;
        margin-right: 30px;
        img{
          height: 100%;
          width: 100%;
          border: 1px solid #98A2A2;
          border-radius: 50%;
        }
      }
      .navbar-start{
        a{
          color: #fff;
        }
      }
      a{
        color: #8E8E8E;
        padding-left: 15px;
        padding-right: 15px;
        font-weight: 300;
        &:hover{
          color: #ffffff;
          background-color: transparent;
        }
      }
    }
    #effects{
      #effect-left{
        top: 200px;
        left: -300px;
        position: absolute;
        height: 120px;
        width: 465px;
        background-image: url("/effect-left.svg");
        @media screen and (max-width: 625px) {
          display: none;
        }
      }
      #effect-top{
        display: none;
        top: -70px;
        right: -275px;
        position: absolute;
        height: 120px;
        width: 465px;
        transform: rotate(335deg);
        background-image: url("/effect-left.svg");
        @media screen and (max-width: 450px) {
          display: none;
        }
      }
    }
  }
</style>

