<template>
  <section>
    <div class="container">
      <h2 class="about-us-title">
        Наша компания специализируется на комплексных поставках трубной продукции для нефтегазовой, химической и
        горнодобывающей отрасли.
      </h2>
      <div class="timeline-wrapper">
        <div class="timeline">
          <h3 class="timeline-header">2012</h3>
          <p class="timeline-text">Специализация на выполнении научно-исследовательских и аналитических работ в области
            геологии и недропользования.</p>
        </div>
        <div class="timeline">
          <h3 class="timeline-header">2014</h3>
          <p class="timeline-text">Выполнены работы по составлению индустриально-инновационного проекта и обоснованию
            ввода во вторичную разработку законсервированных месторождений Шубаркудык и Жаксымай с трудноизвлекаемыми
            запасами в Актюбинской области. Выполнено обоснование открытия месторождения природного газа Тасоюк с
            запасами не менее 50 млрд. м3 в юго-восточной части территории Мангистауской области.</p>
        </div>
        <div class="timeline">
          <h3 class="timeline-header">2018</h3>
          <p class="timeline-text">Получена государственная лицензия на проектирование (технологическое) и
            эксплуатацию горных производств (углеводородное сырье), нефтехимических производств, эксплуатацию
            магистральных газопроводов, нефтепроводов, нефтепродуктопроводов в сфере нефти и газа.</p>
        </div>
        <div class="timeline">
          <h3 class="timeline-header">2019</h3>
          <p class="timeline-text">Подготовка проекта по каолиновой глине месторождений «Союзное» и «Ярославское»,
            проект об освоении промышленных запасов Мугоджарского месторождения кварцевых стекольных песков, проект
            «Утилизация золошлаковых отходов законсервированного золоотвала АО «Актобе ТЭЦ».</p>
        </div>
        <div class="timeline">
          <h3 class="timeline-header">2021 год</h3>
          <p class="timeline-text">Изучая технологические проекты компаний топливно-энергетического комплекса и
            проекты модернизации предприятий нашими опытными специалистами, отлично зная специфику трубной продукции и
            потребности наших клиентов, было принято решение о создании производственно-торгующей компании ТОО
            «Alphamet». Заключены контракты и налажены поставки трубной продукции и трубопроводной арматуры от ведущих
            заводов изготовителей России, Европы и стран ближнего зарубежья. определены основные потребности
            промышленных компаний, налажено производство труб с антикоррозийным и теплогидроизоляционными
            покрытиями.</p>
        </div>
      </div>
    </div>
  </section>

</template>

<style scoped>

p {
  margin:0;
  line-height: 1.4rem;
}

.about-us-title {
  text-align: center;
  margin:2rem auto;
  width:100%;
  max-width:80%;
  font-weight: normal;
  font-size: 2rem;
}
.timeline-wrapper {
  position: relative;
  width:100%;
  max-width:90%;
  margin: 0 auto;
}
.timeline-wrapper:after {
  content: '';
  background:#33337b;
  width:3px;
  height: 3px;
  position: absolute;
  top:0;
  left:-50px;
  height:100%;
}

.timeline-wrapper .timeline {
  padding-bottom: 1.5rem;
  border-bottom: #33337b dashed 2px;
}

.timeline-wrapper .timeline:last-child {
  border:none;
}

.timeline-wrapper .timeline .timeline-header {
  margin-bottom: 0.5rem;
}

@media (max-width:767.98px) {
  .about-us-title {
    max-width: 80%;
    font-size: 1.5rem;
  }
  .timeline-wrapper:after {
    width:100%;
    height:3px;
    left:0;
  }

  .timeline-wrapper .timeline:first-child {
    padding-top:1.5rem;
  }

}


</style>