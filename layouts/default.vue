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
        <a 
          :class="{'navbar-burger': true,'burger': true,'is-active': isResponsive}"
          role="button"
          aria-label="menu"
          aria-expanded="false"
          data-target="navbarBasicExample"
          @click="isResponsive = !isResponsive">
          <span aria-hidden="true"/>
          <span aria-hidden="true"/>
          <span aria-hidden="true"/>
        </a>
      </div>

      <div 
        id="navbarBasicExample"
        :class="{'navbar-menu': true,'is-active': isResponsive}">
        <div class="navbar-start">
          <a 
            class="navbar-item"
            href="https://www.facebook.com/luizotavior18">
            <b-icon 
              icon="facebook-box"/>
          </a>
          <a 
            class="navbar-item"
            href="https://github.com/luizotavior">
            <b-icon 
              icon="github-circle"/>
          </a>
          <a 
            class="navbar-item"
            href="https://www.linkedin.com/in/luizotavior/">
            <b-icon 
              icon="linkedin"/>
          </a>
        </div>

        <div class="navbar-end">
          <a 
            class="navbar-item"
            href="#start"
            @click="isModal = true">Inicio</a>
          <a 
            class="navbar-item"
            href="#about"
            @click="isModal = true">Sobre</a>
          <a 
            class="navbar-item"
            href="#carrer"
            @click="isModal = true">Carreira</a>
          <a 
            class="navbar-item"
            href="#skills"
            @click="isModal = true">Habilidades</a>
          <a 
            class="navbar-item"
            href="#portfolio"
            @click="isModal = true">Portfólio</a>
          <a 
            class="navbar-item"
            href="#contact"
            @click="isModal = true">Contato</a>
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
    <b-modal
      :active.sync="isModal"
      :width="640"
      scroll="keep">
      <div class="card">
        <div class="card-image">
          <figure class="image is-4by3">
            <img 
              src="https://www.febracis.com.br/wp/wp-content/uploads/2018/05/sao-jose-dos-campos-carlos-nava-castillo.jpg"
              alt="Image">
          </figure>
        </div>
        <div class="card-content">
          <div class="media">
            <div class="media-left">
              <figure class="image is-48x48">
                <img 
                  src="/luiz.jpg"
                  alt="Image">
              </figure>
            </div>
            <div class="media-content">
              <p class="title is-4">Luiz Otávio Rodrigues</p>
              <p class="subtitle is-6">@luizotavior</p>
            </div>
          </div>

          <div class="content">
            Olá! Infelizmente meu portfolio não se encontra finalizado. Entretanto, caso deseje você pode fazer download do <a href="/Curriculum_LuizOtavio.pdf">curriculum</a> ou entrar em contato comigo atraves do meu e-mail <a href="mailto:luiz.otavior18@gmail.com">luiz.otavior18@gmail.com</a> respondo rapidamente.<br>Obrigado pela sua visita ! <br> Abraços,
            <br>
            <small>15:33 PM - 25 Nov 2018</small>
          </div>
        </div>
      </div>
    </b-modal>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isModal: false,
      isResponsive: false,
    }
  }
}
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css?family=Poppins:300,400,700');
  html {
    height: 100%;
    width: 100%;
  }
  body {
    min-height: 100%;
    width: 100%;
    background-color: #373841;
  }
  #layout-default{
    font-family: 'Poppins', sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    overflow: hidden;
    .navbar{
      &.is-normal{
        background-color: transparent;
      }
      @media screen and (max-width: 1024px) {
        width: 90%;
        margin-top: 20px;
      }
      @media screen and (min-width: 1024px) {
        background-color: transparent;
        width: 70%;
        min-width: 1024px;
        margin-top: 50px;
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

