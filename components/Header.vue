<template>
  <header>
    <nuxt-link id="logo-wrapper" to="home">
      <img id="logo" src="shared/logo.svg" alt="Logo" />
    </nuxt-link>
    <nav :class="navToggle">
      <span id="close-icon" @click="closeNav">
        <img src="shared/icon-close.svg" alt="close" />
      </span>
      <ul id="menu-list">
        <li v-for="path in paths" :key="path.id" class="menu-item">
          <nuxt-link class="menu-link" :to="path.name">
            <b>{{ path.id }}</b>
            <span>{{ path.name.toUpperCase() }}</span>
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
      paths: [
        { name: 'home', id: '00' },
        { name: 'destination', id: '01' },
        { name: 'crew', id: '02' },
        { name: 'technology', id: '03' },
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
  position: fixed;
  justify-content: space-between;
  display: flex;
  width: 100%;
}

#logo-wrapper {
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
  font-size: 16px;
  line-height: 19px;
  letter-spacing: 2.7px;
}

.menu-link span {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 16px;
  line-height: 19px;
  letter-spacing: 2.7px;
}

#menu-icon-wrapper {
  height: 21px;
  width: 24px;
  margin: 33px 24px;
}
</style>
