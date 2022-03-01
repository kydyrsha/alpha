<template>
  <header>
    <nav class="navbar">
      <RouterLink class="logo-link" to="/"><img class="navbar-logo" src="@/assets/images/alphamet-logo-no-border.png"
                                                alt="logo"></RouterLink>
<!--      <div class="mobile-links">-->
<!--        <a href="tel:+77006055555">          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="20" height="20">-->
<!--          <path fill="none" d="M0 0h24v24H0z"/>-->
<!--          <path-->
<!--              d="M21 16.42v3.536a1 1 0 0 1-.93.998c-.437.03-.794.046-1.07.046-8.837 0-16-7.163-16-16 0-.276.015-.633.046-1.07A1 1 0 0 1 4.044 3H7.58a.5.5 0 0 1 .498.45c.023.23.044.413.064.552A13.901 13.901 0 0 0 9.35 8.003c.095.2.033.439-.147.567l-2.158 1.542a13.047 13.047 0 0 0 6.844 6.844l1.54-2.154a.462.462 0 0 1 .573-.149 13.901 13.901 0 0 0 4 1.205c.139.02.322.042.55.064a.5.5 0 0 1 .449.498z"-->
<!--              fill="rgba(255,255,255,1)"/>-->
<!--        </svg>-->
<!--        </a>-->
<!--      </div>-->
      <a href="#" class="toggle-button" @click="toggleMenu">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </a>
      <ul class="menu" :class="{'active': isActive}">
        <RouterLink class="menu-link" to="/">Главная</RouterLink>
        <RouterLink class="menu-link" to="/about">О нас</RouterLink>
        <RouterLink class="menu-link" to="/product">Продукция</RouterLink>
        <RouterLink class="menu-link" to="/charity">Благотворительность</RouterLink>
        <RouterLink class="menu-link" to="/contacts">Контакты</RouterLink>
      </ul>
      <div class="navbar-links">
        <a class="phone" href="tel:+77006055555">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="20" height="20">
            <path fill="none" d="M0 0h24v24H0z"/>
            <path
                d="M21 16.42v3.536a1 1 0 0 1-.93.998c-.437.03-.794.046-1.07.046-8.837 0-16-7.163-16-16 0-.276.015-.633.046-1.07A1 1 0 0 1 4.044 3H7.58a.5.5 0 0 1 .498.45c.023.23.044.413.064.552A13.901 13.901 0 0 0 9.35 8.003c.095.2.033.439-.147.567l-2.158 1.542a13.047 13.047 0 0 0 6.844 6.844l1.54-2.154a.462.462 0 0 1 .573-.149 13.901 13.901 0 0 0 4 1.205c.139.02.322.042.55.064a.5.5 0 0 1 .449.498z"
                fill="rgba(255,255,255,1)"/>
          </svg>
          +7-700-605-55-55
        </a>
        <a class="email" href="mailto:info@alphamet.kz">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="20" height="20">
            <path fill="none" d="M0 0h24v24H0z"/>
            <path
                d="M3 3h18a1 1 0 0 1 1 1v16a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1zm17 4.238l-7.928 7.1L4 7.216V19h16V7.238zM4.511 5l7.55 6.662L19.502 5H4.511z"
                fill="rgba(255,255,255,1)"/>
          </svg>
          info@alphamet.kz
        </a>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isActive: false
    }
  },
  methods: {
    toggleMenu () {
      this.isActive = !this.isActive
    }
  }
}
</script>
<style scoped>
.navbar {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.navbar .logo-link {
  display: flex;
}

.navbar .navbar-logo {
  width: 100%;
  max-width: 150px;
}

.navbar .toggle-button {
  position: absolute;
  top: 0.75rem;
  right: 1rem;
  display: none;
  flex-direction: column;
  justify-content: space-between;
  width: 30px;
  height: 21px;
}

.navbar .toggle-button .bar {
  height: 3px;
  width: 100%;
  background-color: #fff;
  border-radius: 10px;
}

.navbar .menu {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.navbar .menu .menu-link {
  color: #fff;
  padding: 1rem;
  display: block;
  transition: 0.6s;
}

.navbar .menu .menu-link:hover {
  background-color: #2e2e61;
}

.navbar .navbar-links > a {
  text-decoration: none;
  color: #fff;
  display: flex;
  flex-direction: row;
  align-items: center;
  transition: 0.6s;
}

.navbar .navbar-links > a:hover {
  opacity: 0.7;
}

.navbar .navbar-links > a > svg {
  margin-right: 0.5rem;
}

.navbar .navbar-links {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.navbar .navbar-links .phone {
  margin-right: 1rem;
}


@media (max-width: 480px) {
  .navbar .toggle-button {
    display: flex;
  }

  .navbar .menu {
    display: none;
    width: 100%;
    flex-direction: column;
  }

  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .navbar-links .menu {
    width: 100%;
    flex-direction: column;
  }

  .navbar .menu li {
    text-align: center;
  }

  .navbar .menu .menu-link {
    padding: 0.5rem 1rem;
  }

  .navbar .menu.active {
    display: flex;
  }

  .navbar .navbar-links {
    display: none;
  }
}
</style>
