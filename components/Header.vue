<template>
  <header>
    <nuxt-link id="header-logo-wrapper" to="/">
      <img id="logo" src="shared/logo.svg" alt="Logo" />
    </nuxt-link>
    <div id="header-line"></div>
    <nav :class="navToggle">
      <div id="header-line"></div>
      <span id="close-icon" @click="closeNav">
        <img src="shared/icon-close.svg" alt="close" />
      </span>
      <ul id="menu-list">
        <li v-for="page in pages" :key="page.id" class="menu-item">
          <nuxt-link class="menu-link" :to="page.path">
            <b>{{ page.id }}</b>
            <span>{{ page.label.toUpperCase() }}</span>
          </nuxt-link>
        </li>
      </ul>
    </nav>
    <span id="menu-icon-wrapper" @click="openNav">
      <img id="menu-icon" src="shared/icon-hamburger.svg" alt="menu-icon" />
    </span>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',

  data() {
    return {
      pages: [
        { label: 'home', id: '00', path: '/' },
        { label: 'destination', id: '01', path: '/destination' },
        { label: 'crew', id: '02', path: '/crew' },
        { label: 'technology', id: '03', path: '/technology' },
      ],
      navToggle: null,
    }
  },

  methods: {
    openNav() {
      this.navToggle = 'nav-opened'
    },
    closeNav() {
      this.navToggle = 'nav-closed'
    },
  },
}
</script>

<style scoped>
header {
  position: absolute;
  display: flex;
  width: 100%;
  justify-content: space-between;
}

#header-logo-wrapper {
  height: 40px;
  width: 40px;
  margin: 24px;
}

#logo {
  height: 100%;
  width: 100%;
}

nav {
  background: rgba(255 255 255 4%);
  backdrop-filter: blur(81.5485px);
  height: 100vh;
  position: fixed;
  right: -254px;
  width: 254px;
}

.nav-closed {
  animation: close-nav forwards 0.6s;
}

@keyframes close-nav {
  from {
    transform: translateX(-100%);
  }

  to {
    transform: translateX(0);
  }
}

.nav-opened {
  animation: open-nav forwards 0.6s;
}

@keyframes open-nav {
  from {
    transform: translateX(0);
  }

  to {
    transform: translateX(-100%);
  }
}

#close-icon {
  position: absolute;
  top: 33.95px;
  right: 26.45px;
}

#menu-list {
  position: absolute;
  top: 100px;
  width: 100%;
}

.menu-item {
  align-items: center;
  display: flex;
  height: 50px;
  letter-spacing: 2.7px;
  padding-left: 32px;
  width: 100%;
}

.menu-link {
  color: #ffff;
  text-decoration: none;
}

.menu-link b {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 1.6rem;
  line-height: 19px;
  letter-spacing: 2.7px;
}

.menu-link span {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 1.6rem;
  line-height: 19px;
  letter-spacing: 2.7px;
}

#menu-icon-wrapper {
  height: 21px;
  width: 24px;
  margin: 33px 24px;
}

@media only screen and (min-width: 600px) {
  #header-logo-wrapper {
    height: 48px;
    width: 48px;
    margin: 24px 39px;
  }

  #menu-icon-wrapper {
    display: none;
  }

  nav {
    right: 0;
    position: absolute;
    width: 450px;
    height: 96px;
  }

  #close-icon {
    display: none;
  }

  #menu-list {
    top: 0;
    height: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
  }

  .menu-link b {
    display: none;
  }

  .menu-item {
    width: auto;
    height: 100%;
    padding: 0;
  }

  .menu-link span {
    font-size: 1.4rem;
  }
}

@media only screen and (min-width: 900px) {
  header {
    min-width: 1445px;
  }

  #header-logo-wrapper {
    margin: 55px;
  }

  #header-line {
    position: absolute;
    top: 43px;
    left: -450px;
    width: 473px;
    height: 1px;
    background: #fff;
    mix-blend-mode: normal;
    opacity: 0.25;
    z-index: 10;
  }

  nav {
    top: 35px;
    right: 0;
    position: relative;
    width: 830px;
    height: 85px;
  }

  .menu-link b {
    display: inline-block;
  }

  .menu-link span {
    font-size: 1.6rem;
  }
}
</style>
