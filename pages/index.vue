<template>
  <section 
    id="start"
    class="section-start">
    <div class="introduction">
      <h1>
        <span class="name">Luiz Otávio</span>
        <span class="family-name">Rodrigues</span>
        <span class="office">Full-Stack Developer</span>
      </h1>
      <a 
        class="introduction-action" 
        href="#">
        Curriculum
      </a>
    </div>
    <luiz-person/>
  </section>
</template>

<script>
  import LuizPerson from '@/components/luiz'
  export default {
    name: 'HomePage',
    components: {
        LuizPerson
    },
    data() {
        return {
        }
    }
  }
</script>

<style lang="scss" scoped>
  section#start{
    width: 100%;
    max-width: 1200px;
    display: flex;
    flex-direction: row;
    align-items: center;
    flex-wrap: wrap;
    justify-content: space-around;
    margin: 50px 0px;
    div.introduction{
      h1{
        display: flex;
        flex-direction: column;
        margin-bottom: 25px;
        span.name{
          font-size: 64px;
          font-weight: 700;
          line-height: 64px;
        }
        span.family-name{
          font-size: 48px;
          font-weight: 700;
          line-height: 48px;
        }
        span.office{
          font-size: 18px;
          font-weight: 300;
        }
      }
      a.introduction-action{
        border: 1px solid #98A2A2;
        padding: 11px 40px;
        border-radius: 30px;
        color: #ffffff;
        &:hover{
          background-color: #ffffff;
          color: #000;
        }
      }
      @media screen and (max-width: 860px) {
        position: absolute;
        bottom: 60px;
      }
    }
 }
</style>
