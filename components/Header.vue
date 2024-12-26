<template>
  <header class="header text-font">
    <div class="logo logo-font">
      <h2><a href="#home">BURGUR CLUB</a></h2>
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
    padding: 30px 100px;
    display: flex;
    align-items: center;
    position: fixed;
    width: 100vw;
    z-index: 1000;
    
    & .logo {

      & > h2 {

        & > a {
          font-size: 40px;
        }
      }
    }

    & > nav {
      display: flex;
      position: absolute;
      right: 100px;
      align-items: center;

      & > ul {
        display: flex;
        gap: 50px;

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