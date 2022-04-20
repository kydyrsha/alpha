<template>
  <section>
    <div class="container">
      <div class="charity-wrapper">
        <div class="dara-charity">
          <a class="dara-link" href="https://dara.kz/">
            <img class="dara-logo" src="@/assets/images/logo-dara.svg" alt="logo-dara">
          </a>
          <div class="dara-content">
            <p class="dara-text">Наша компания является партнером благотворительного фонда <a class="dara-link"
                                                                                              href="https://dara.kz/about/contacts">«Дара»</a>,
              миссией которого является реализация проектов, направленных на улучшение условий жизни и расширение
              возможностей развития детей-сирот и детей с особыми образовательными потребностями.</p>
            <p class="dara-text">Мы уверены, что среди наших партнеров найдутся неравнодушные люди, которые как и мы
              хотят помочь
              фонду.</p>
            <div class="contacts">
              <div class="requisites">
                <h2>Реквизиты:</h2>
                <p>Частный фонд "Дара":</p>
                <p>ИИК KZ3196503F0007778251</p>
                <p>БИК IRTYKZKA</p>
                <p>БИН 050540010390</p>
                <p>Филиал АО "ForteBank" в г. Нур-Султан</p>
              </div>
              <div class="phone">
                <h2>Телефон:</h2>
                <a class="dara-link" href="tel:+77051143250">+7-705-114-32-50</a>
              </div>
              <div class="email">
                <h2>Email:</h2>
                <a class="dara-link" href="mailto:info@dara.kz">info@dara.kz</a>
              </div>
            </div>
          </div>
        </div>
        <img class="dara-charity-img" src="@/assets/images/dara-bg.jpg" width="100%" alt="charity" title="Dara charity">
      </div>
    </div>
  </section>
</template>

<style scoped>
.charity-wrapper .dara-charity {
  display: flex;
  align-items: center;
  padding: 2rem 0;
}

.charity-wrapper .dara-charity .dara-link .dara-logo {
  width: 200px;
  margin-right: 2rem;
}

.dara-link {
  color: #e64926;
}

.contacts {
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  align-items: flex-start;
}

.charity-wrapper .dara-charity .dara-content .dara-text {
  text-align: justify;
}

.dara-charity-img {
  display: block;
  width: 100%;
  margin-bottom: 2rem;
}


@media (max-width: 767.98px) {
  .charity-wrapper .dara-charity {
    flex-direction: column;
    text-align: center;
  }

  .charity-wrapper .dara-charity .dara-link .dara-logo {
    margin: 0;
  }

  .contacts {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}
</style>
