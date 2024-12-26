<template>
  <header class="header text-font">
    <div class="logo logo-font">
      <h2 @click="postCurrentDNS('home')">BURGUR CLUB</h2>
    </div>

    <nav>
      <ul>
        <li @click="postCurrentDNS('home')">Home</li>
        <li @click="postCurrentDNS('menu')">Menu</li>
        <li @click="postCurrentDNS('about')">About</li>
      </ul>
    </nav>
  </header>
</template>

<style lang="less" scoped>
  .header {
    padding: 20px 100px;
    display: flex;
    align-items: center;
    position: fixed;
    width: 100vw;
    z-index: 1000;

    @media(max-width: 600px) {
      padding: 30px 20px;

    }
    
    & .logo {

      & > h2 {
        cursor: pointer;
        font-size: 40px;
        @media(max-width: 600px) {
          font-size: 20px;
          width: 130px;
        }
      }
    }

    & > nav {
      display: flex;
      position: absolute;
      right: 100px;
      align-items: center;
      
      @media(max-width: 600px) {
        right: 20px;

      }
      & > ul {
        display: flex;
        @media(max-width: 600px) {
          gap: 10px;
          
        }
        gap: 30px;

        & > li {
          cursor: pointer;
          & > a {
            font-size: 20px;
          }
        }
      }
    }
  }
</style>

<script setup>
  const router = useRouter();
  router.replace({ path: `/` });
  function postCurrentDNS(name) {
    router.replace({ path: `/${name}` });
    if(name == 'home') {
      scrollTo(0,0)      
    } else if (name == 'menu') {
      scrollTo(0,300)      
      
    } else if (name == 'about') {
      scrollTo(0,700)      

    }
    setTimeout(() => {
      router.replace({ path: `/` }); 
    },500)

  }

</script>