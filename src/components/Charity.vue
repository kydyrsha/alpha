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
              миссией которого является реализация проектов, направленных на помощь детским медицинским учреждениям,
              детским домам, а также школам-интернатам для детей с ограниченными возможностями. Свою деятельность «Дара»
              осуществляет для улучшения условий жизни и расширения возможностей развития детей-сирот, детей с
              ограниченными возможностями и больных детей.</p>
            <p class="dara-text">Мы уверены, что среди наших партнеров найдутся неравнодушные люди, которые как и мы хотят помочь
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
        <img src="src/assets/images/dara-bg.jpg" width="100%" alt="charity  ">
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
  display:flex;
  justify-content: space-between;
  flex-direction: row;
  align-items: flex-start;
}

.charity-wrapper .dara-charity .dara-content .dara-text {
  text-align: justify;
}

@media (max-width: 767.98px) {
  .charity-wrapper .dara-charity {
    flex-direction: column;
    text-align: center;
  }

  .charity-wrapper .dara-charity .dara-link .dara-logo {
    margin: 0;
  }
}
</style>