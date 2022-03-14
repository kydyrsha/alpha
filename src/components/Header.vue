<template>
  <header>
    <div class="banner-bg">
      <video class="alphamet-intro" autoplay loop muted playsinline>
        <source src="@/assets/video/alphamet.mp4" type="video/mp4" />
      </video>
      <div class="banner-text">
        <h1 class="title">Компания Alphamet</h1>
        <h2 class="sub-title">Комплексные решения для нефтехимической<Br/>и горнодобывающей отрасли</h2>
      </div>
    </div>
    <nav class="navbar">
      <RouterLink class="logo-link" to="/"><img class="navbar-logo" src="@/assets/images/alphamet-transparent.png"
                                                alt="logo"></RouterLink>
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
        <div class="phones">
          <a class="phone" href="tel:+77273270087">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="20" height="20">
              <path fill="none" d="M0 0h24v24H0z"/>
              <path
                  d="M21 16.42v3.536a1 1 0 0 1-.93.998c-.437.03-.794.046-1.07.046-8.837 0-16-7.163-16-16 0-.276.015-.633.046-1.07A1 1 0 0 1 4.044 3H7.58a.5.5 0 0 1 .498.45c.023.23.044.413.064.552A13.901 13.901 0 0 0 9.35 8.003c.095.2.033.439-.147.567l-2.158 1.542a13.047 13.047 0 0 0 6.844 6.844l1.54-2.154a.462.462 0 0 1 .573-.149 13.901 13.901 0 0 0 4 1.205c.139.02.322.042.55.064a.5.5 0 0 1 .449.498z"
                  fill="rgba(255,255,255,1)"/>
            </svg>
            +7-727-327-00-87
          </a>
          <a class="phone" href="tel:+77058073742">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="20" height="20">
              <path fill="none" d="M0 0h24v24H0z"/>
              <path
                  d="M21 16.42v3.536a1 1 0 0 1-.93.998c-.437.03-.794.046-1.07.046-8.837 0-16-7.163-16-16 0-.276.015-.633.046-1.07A1 1 0 0 1 4.044 3H7.58a.5.5 0 0 1 .498.45c.023.23.044.413.064.552A13.901 13.901 0 0 0 9.35 8.003c.095.2.033.439-.147.567l-2.158 1.542a13.047 13.047 0 0 0 6.844 6.844l1.54-2.154a.462.462 0 0 1 .573-.149 13.901 13.901 0 0 0 4 1.205c.139.02.322.042.55.064a.5.5 0 0 1 .449.498z"
                  fill="rgba(255,255,255,1)"/>
            </svg>
            +7-705-807-37-42
          </a>
        </div>
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
    toggleMenu() {
      this.isActive = !this.isActive
    }
  }
}
</script>
<style scoped>
header {
  position: relative;
  height:100vh;
  max-height:700px;
}

.banner-bg::after {
  content: '';
  position: absolute;
  width:100%;
  height:100%;
  max-height: 700px;
  background-color: rgba(0, 0, 0, 0.3);
  top:0;
  right: 0;
  z-index: 3;
}

.banner-text {
  position: absolute;
  top:30%;
  left:22%;
  color:#fff;
  z-index: 5;
}

.banner-text .title {
  font-size: 2.5rem;
  letter-spacing: 0.1rem;
  margin:0.5rem 0;
}

.banner-text .sub-title {
  font-weight: normal;
  letter-spacing: 0.05rem;
  margin:0.5rem 0;
  font-size: 2rem;
}

@media (max-width:767.98px) {
  .alphamet-intro {
    min-height: 500px;
  }

  .banner-text {
    top:35%;
    left:0%;
  }

  .banner-text .sub-title {
    font-size: 1.75rem;
    text-align: center;
  }

  .banner-text .title {
    text-align: center;
  }

}

header .alphamet-intro {
  position: absolute;
  top:0;
  right:0;
  height:100vh;
  width:100vw;
  max-height: 700px;
  object-fit: cover;
}

.navbar {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  height: 80px;
  position: sticky;
  z-index: 5;
}

.navbar .logo-link {
  display: flex;
}

.navbar .navbar-logo {
  width: 100%;
  max-width: 180px;
}

.navbar .toggle-button {
  position: absolute;
  top: 1.25rem;
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
  opacity: 0.7;
}

.navbar .navbar-links a {
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

.navbar .navbar-links .phones {
  display: flex;
  flex-direction: column;
}

.navbar .navbar-links .phone {
  margin-right: 1rem;
}

.navbar .navbar-links .phone:first-child {
  margin-bottom: 0.5rem;
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
