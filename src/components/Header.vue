<template>
  <header class="main-header">
    <nav class="navbar desktop">
      <RouterLink class="logo-link" to="/"><img class="navbar-logo" src="@/assets/images/alphamet-transparent.png"
                                                alt="logo" title="Alphamet logo"></RouterLink>
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
<!--      <a class="menu-link active" href="#">перезвоните мне</a>-->
      <RouterLink class="menu-link active" to="/">перезвоните мне</RouterLink>
    </nav>

    <nav class="navbar mobile">
      <div class="burger" @click="toggleMenu()">
        <span></span>
      </div>
      <RouterLink class="logo-link" to="/"><img class="navbar-logo" src="@/assets/images/alphamet-transparent.png"
                                                alt="logo" title="Alphamet logo"></RouterLink>
      <ul class="menu" :class="{'active': isActive}">
        <RouterLink class="menu-link" to="/">Главная</RouterLink>
        <RouterLink class="menu-link" to="/about">О нас</RouterLink>
        <RouterLink class="menu-link" to="/product">Продукция</RouterLink>
        <RouterLink class="menu-link" to="/charity">Благотворительность</RouterLink>
        <RouterLink class="menu-link" to="/contacts">Контакты</RouterLink>
      </ul>
<!--      <a class="menu-link active" href="#">перезвоните мне</a>-->
      <RouterLink class="menu-link active" to="/">перезвоните мне</RouterLink>
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
.main-header {
  background: var(--brand-blue);
  position: fixed;
  top:0;
  z-index: 200;
  width:100%;
  height: 110px;
}

header .menu-link {
  color: var(--brand-white);
  transition: 0.6s;
  display: flex;
  text-decoration: none;
  padding: 0.5rem 1.25rem;
}

header .menu-link:hover {
  background: rgba(238, 75, 43, 0.9);
  border-radius: 1.25rem;
}

header .menu-link.active:hover {
  color: var(--brand-white);
  background: rgba(238, 75, 43, 0.9);
  border-radius: 1.25rem;
  animation: none;
}

header .menu-link.active {
  transition: 0.6s;
  background: rgba(238, 75, 43, 1);
  color: #fff;
  border-radius: 0.75rem;
  animation: pulse 2s infinite;
  box-shadow: 0 0 0 0 rgba(238, 75, 43, 1);
  font-size: 22px;
  letter-spacing: 1px;
  font-weight: 300;
}

@keyframes pulse {
  0% {
    transform: scale(0.95);
    box-shadow: 0 0 0 0 rgba(238, 75, 43, 0.7);
  }

  70% {
    transform: scale(1);
    box-shadow: 0 0 0 10px rgba(238, 75, 43, 0);
  }

  100% {
    transform: scale(0.95);
    box-shadow: 0 0 0 0 rgba(238, 75, 43, 0);
  }
}

.main-header nav {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1.5rem 0;
}

.main-header .logo-link {
  width: 100%;
  display: flex;
  max-width: 180px;
}

.main-header .menu {
  display: flex;
  justify-content: space-between;
  width: 100%;
  max-width: 700px;
}

.main-header .menu-link {
  color: var(--brand-white);
  transition: 0.6s;
  display: flex;
  text-decoration: none;
  padding: 0.5rem 1.25rem;
}

.main-header .menu-link:hover {
  background: rgba(238, 75, 43, 0.9);
  border-radius: 1.25rem;
}

.main-header .menu-link.active:hover {
  color: var(--brand-white);
  background: rgba(238, 75, 43, 1);
  border-radius: 1.25rem;
  animation: none;
}

@keyframes pulse {
  0% {
    transform: scale(1);
    box-shadow: 0 0 0 0 rgba(238, 75, 43, 0.8);
  }

  50% {
    transform: scale(1);
    box-shadow: 0 0 0 15px rgba(238, 75, 43, 0);
  }

  100% {
    transform: scale(1);
    box-shadow: 0 0 0 0 rgba(238, 75, 43, 0);
  }
}


.main-header .contacts-link > svg {
  margin-right: 0.5rem;
  width: 20px;
  height: auto;
  transition: 0.6s;
}

.navbar {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
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
  background-color: var(--brand-white);
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
  color: var(--brand-white);
  display: block;
  transition: 0.6s;
}

.navbar .navbar-links a {
  text-decoration: none;
  color: var(--brand-white);
  display: flex;
  flex-direction: row;
  align-items: center;
  transition: 0.6s;
}


.navbar .navbar-links > a > svg {
  margin-right: 0.5rem;
}

.navbar .navbar-links {
  display: flex;
  flex-direction: row;
  align-items: center;
}

@media (min-width:1300px) {
  .navbar.desktop {
    display:flex;
  }

  .navbar.mobile {
    display:none;
  }
}

@media (max-width: 1299.98px) {

  .main-header .logo-link {
    display:none;
  }

  .navbar.desktop {
    display:none;
  }

  .main-header {
    height:110px;
  }

  .navbar.mobile {
    display:flex;
    flex-direction: row;
    width:100%;
    max-width:90%;
    padding:1.5rem 0;
    height:100%;
  }

  .navbar.mobile .burger {
    z-index: 20;
    display: block;
    position: relative;
    width:35px;
    height:20px;
    cursor: pointer;
  }

  .navbar.mobile .burger > span,
  .navbar.mobile .burger:before,
  .navbar.mobile .burger:after {
    left:0;
    position: absolute;
    height: 10%;
    width:100%;
    transition: all 0.3s ease 0s;
    background-color: var(--brand-white);
  }

  .navbar.mobile .burger:before,
  .navbar.mobile .burger:after {
    content: '';
  }

  .navbar.mobile .burger:before {
    top:0;
  }

  .navbar.mobile .burger:after {
    bottom:0;
  }

  .navbar.mobile .burger > span {
    top:50%;
    transform: scale(1) translate(0px,-50%);
  }

  .navbar.mobile .menu {
    position: fixed;
    top:0;
    left:0;
    width:100%;
    transform: translate(-100%,0px);
    background-color: rgba(0,71,171,1);
    transition: all 0.3s ease 0s;
    margin-top: 110px;
    color: var(--brand-white);
  }

  .navbar.mobile .menu.active {
    transform: translate(0px,0px);
  }

  .main-header .menu {
    max-width:100%;
  }

  .main-header nav {
    padding:0;
  }

  .navbar .toggle-button {
    display: flex;
  }

  .navbar .menu {
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
    border-radius: unset;
  }

  .navbar .menu.active {
    display: flex;
  }

  .navbar .navbar-links {
    display: none;
  }
}
</style>
