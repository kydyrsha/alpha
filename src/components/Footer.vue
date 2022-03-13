<template>
  <footer>
    <div class="container">
      <div class="footer-wrapper">
        <div class="useful-links">
          <h2 class="useful-header">Полезные ссылки:</h2>
          <ul class="menu">
            <RouterLink class="menu-link" to="/">Главная</RouterLink>
            <RouterLink class="menu-link" to="/about">О нас</RouterLink>
            <RouterLink class="menu-link" to="/product">Продукция</RouterLink>
            <RouterLink class="menu-link" to="/charity">Благотворительность</RouterLink>
            <RouterLink class="menu-link" to="/contacts">Контакты</RouterLink>
          </ul>
        </div>
        <div class="contact-us">
          <h2 class="contact-us-header">
            Свяжитесь с нами:
          </h2>
          <div class="contacts">
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
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
name: "Footer"
}
</script>

<style scoped>
footer {
  background: #002f6c;
}

.menu {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

h2 {
  color:#fff;
  padding:1rem;
  margin:0;
  font-weight: normal;
}

.menu .menu-link {
  color: #fff;
  padding: 1rem;
  display: block;
  transition: 0.6s;
}

.menu .menu-link:hover {
  opacity:0.7;
}

footer .footer-wrapper {
  display:flex;
  justify-content: space-between;
}

.contact-us .contacts {
  display: flex;
  flex-direction: column;
}

.contact-us .contacts > a {
  padding: 1rem;
  display: flex;
  align-items: center;
  color:#fff;
  transition: 0.6s;
}

.contact-us .contacts > a:hover {
  opacity: 0.7;
}

.contact-us .contacts > a > svg {
  margin-right: 1rem;
}

@media (max-width:767.98px) {
  footer .footer-wrapper {
    flex-direction: column;
  }

  h2 {
    font-size: 2rem;
  }
}

.phones {
  display: flex;
  flex-direction: column;
}

.phones a {
  color:#fff;
  align-items: center;
  display: flex;
  transition: 0.7s;
}

.phones a:hover {
  opacity:0.7;
}

.phone {
  padding:1rem;
}

.phone svg {
  margin-right: 0.5rem;
}
</style>
