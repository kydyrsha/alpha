<template>
  <section class="engineering">
    <h1 class="visually-hidden">Главный поставщик металлопроката в Казахстане</h1>
    <div class="container">
      <h2 class="engineering-header">Комплексный подход</h2>
      <div class="engineering-wrapper">
        <div class="engineering-block">
          <img src="@/assets/images/services/sketch.png" alt="sketch-icon">
          <p>Проектирование (технологическое) нефтехимических производств</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/services/block3.png" alt="paper-icon">
          <p>Составление технико-экономического обоснования проектов для месторождений углеводородного сырья</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/services/tubes.png" alt="pipe-icon">
          <p>Поставка труб различных диаметров и марок стали</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/services/laboratory.png" alt="lab-icon">
          <p>Поставка промышленного и технического оборудования</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/services/corrosive.png" alt="corrosive-icon">
          <p>Антикоррозийное покрытие</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/services/maintenance.png" alt="lab-icon">
          <p>Строительно-монтажные работы</p>
        </div>
      </div>
    </div>
  </section>
  <section class="facts">
    <div class="container">
      <div class="facts-wrapper">
        <h2 class="facts-header"><span>Более <b>10</b> контрактов</span><br>с ведущими заводами в своих отраслях</h2>
        <img class="hs-img" src="@/assets/images/handshake.png" alt="handshake">
      </div>
    </div>
  </section>
  <section class="advantages">
    <div class="container">
      <h2 class="advantages-header">
        Ваши преимущества<br>
        <span>от работы с ТОО "Alphamet"</span></h2>
      <div class="advantages-wrapper">
        <div class="advantage">
          <img src="@/assets/images/services/1.svg" alt="1">
          <h3>Проектирование</h3>
          <p>Осуществление полного комплекса работ в области разработки проектной документации на всех  стадиях проектирования</p>
        </div>
        <div class="advantage">
          <img src="@/assets/images/services/2.svg" alt="2">
          <h3>Поставка материалов и оборудования</h3>
          <p>Комплексный подход от подбора строительных материалов до промышленного оборудования</p>
        </div>
        <div class="advantage">
          <img src="@/assets/images/services/3.svg" alt="3">
          <h3>Сдача объекта в эксплуатацию</h3>
          <p>Сдача объекта в эксплуатацию</p>
        </div>
      </div>
    </div>
  </section>
</template>


<style scoped>

.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  border: 0;
  padding: 0;
  white-space: nowrap;
  clip-path: inset(100%);
  clip: rect(0 0 0 0);
  overflow: hidden;
}
section:after {
  content: '';
  position: absolute;
  width:100%;
  height:8px;
  background: linear-gradient(to right, #002f6c, #2cd5c4);
}

h2 {
  font-weight: normal;
  font-size: 2rem;
}

p {
  line-height: 1.5rem;
  text-align: center;
}

.banner {
  position: relative;
}

.banner-bg::after {
  content: '';
  position: absolute;
  width:100%;
  height:100%;
  max-height: 520px;
  background-color: rgba(0, 0, 0, 0.6);
  top:0;
  right: 0;
}

.banner .banner-text {
  position: absolute;
  top:30%;
  left:20%;
  color:#fff;
}

.banner .banner-text .title {
  font-size: 2.5rem;
  letter-spacing: 0.1rem;
  margin:0.5rem 0;
}

.banner .banner-text .sub-title {
  font-weight: normal;
  letter-spacing: 0.05rem;
  margin:0.5rem 0;
  font-size: 2rem;
}

.banner .alphamet-intro {
  width:100%;
  max-height: 520px;
  height:100%;
  object-fit: cover;
  display:block;
}

@media (max-width:767.98px) {
  .banner .alphamet-intro {
    min-height: 500px;
  }
  .banner .banner-text {
    top:10%;
    left:5%;
  }

}

.engineering .engineering-header {
  text-align: center;
  font-size: 2rem;
  padding:2.5rem 0;
  margin:0;
  letter-spacing: 1px;
  font-weight: normal;
}

.engineering .engineering-wrapper {
  display:flex;
  justify-content: space-between;
  flex-wrap: wrap;
  position: relative;
  padding-bottom: 2rem;
}

.engineering .engineering-wrapper .engineering-block {
  width:33%;
  display:flex;
  align-items: center;
  flex-direction: column;
}

.engineering .engineering-wrapper .engineering-block > img {
  width:20%;
  margin-bottom: 1rem;
}

.engineering .engineering-wrapper .engineering-block > p {
  width:80%;
}

@media (max-width: 767.98px) {
  .engineering .engineering-wrapper {
    flex-direction: column;
  }

  .engineering .engineering-wrapper .engineering-block {
    width:100%;
    margin-bottom: 3rem;
  }

  .engineering .engineering-wrapper .engineering-block > img {
    width:20%;
  }

  .engineering .engineering-wrapper .engineering-block > p {
    width:75%;
  }
}

.facts {
  position: relative;
  background-color: #002f6c;
  margin-bottom: 2rem;
}

.facts .facts-wrapper {
  display:flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

.facts .facts-wrapper .hs-img {
  width:40%;
}

.facts .facts-wrapper .facts-header {
  color:#fff;
  text-align: center;
  font-weight: normal;
  margin:0;
  width:60%;
}

.facts .facts-wrapper .facts-header > span {
  font-size: 3rem;
}

@media (max-width:767.98px) {
  .facts .facts-wrapper {
    flex-direction: column;
  }

  .advantages .advantages-wrapper .advantage {
    width:100%;
  }

  .advantages .container {
    padding:0;
  }
}

.advantages {
  padding: 2rem 0;
  /*background: #002f6c;*/
  /*margin-bottom: 2rem;*/
}

.advantages:after {
  content: none;
}

.advantages .advantages-wrapper {
  display: flex;
  align-items: flex-start;
  justify-content: center;
  flex-direction: row;
}

.advantages .advantages-header {
  text-align: center;
  font-size: 3rem;
  line-height: 2.75rem;
  color:#000;
  margin:0;
  padding-bottom: 2rem;
}

.advantages .advantages-header > span {
  font-size: 2.25rem;
}

.advantages .advantages-wrapper .advantage {
  display:flex;
  flex-direction: column;
  align-items: center;
  color:#fff;
  width:400px;
  height:270px;
  justify-content: center;
}

.advantages .advantages-wrapper .advantage > h3 {
  font-size: 1.5rem;
  margin:0;
  text-align: center;
}

.advantages .advantages-wrapper .advantage > p {
  padding:1rem;
  margin:0;
}

.advantages .advantages-wrapper .advantage:first-child {
  background: #064499;
}
.advantages .advantages-wrapper .advantage:nth-child(3n-1) {
  background: #3567b0;
}

.advantages .advantages-wrapper .advantage:last-child {
  background: #e72120;
}

.advantages .advantages-wrapper .advantage > img {
  width:100px;
  height:100px;
}

@media (max-width:767.98px) {
  .advantages .advantages-wrapper {
    flex-direction: column;
  }

  .advantages .advantages-wrapper .advantage {
    width:100%;
  }

  .advantages .advantages-header {
    font-size: 2.5rem;
    padding:0.5rem;
    padding-bottom: 2rem;
  }

  .facts {
    margin-bottom: 0;
  }

}
</style>
