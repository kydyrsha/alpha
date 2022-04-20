<template>
  <header class="main-header">
    <nav class="navbar">
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
      <div class="navbar-links">
        <a class="menu-link active" href="#">перезвоните мне</a>
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

.main-header {
  background: var(--brand-blue);
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
  max-width: 200px;
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
