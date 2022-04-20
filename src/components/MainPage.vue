<template>
  <h1 class="visually-hidden">Главный поставщик металлопроката в Казахстане</h1>
  <section class="banner-bg">
    <picture>
      <source srcset="src/assets/images/banner.webp" type="image/webp" title="stack of pipes">
      <img src="@/assets/images/banner.jpg" alt="pipes" title="stack of pipes">
    </picture>
    <div class="banner-text">
      <h2 class="title">Компания Alphamet</h2>
      <h3 class="sub-title">Комплексные решения для нефтехимической<Br/>и горнодобывающей отрасли</h3>
    </div>
  </section>
  <section class="engineering">
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
  <a class="cta" href="tel:+77006055555"><img class="active" src="@/assets/images/ringing.png" alt="phone-icon" title="call"></a>
</template>


<style scoped>


.cta {
  position: fixed;
  right: 3%;
  bottom: 5%;
}

.cta > img {
  width:100%;
  max-width:100px;
  background-color: var(--brand-red);
  border-radius: 50%;
  padding:1rem;
  animation: ringing;
  animation-duration: 2.25s;
  animation-iteration-count: infinite;
  transition: 0.7s;
}

@keyframes ringing {
  0% {
    transform: rotate(-60deg);
    box-shadow: 0 0 0 0 rgba(238, 75, 43, 0.8);
  }

  50% {
    transform: rotate(-20deg);
    box-shadow: 0 0 0 15px rgba(238, 75, 43, 0);
  }

  100% {
    transform: rotate(20deg);
    box-shadow: 0 0 0 0 rgba(238, 75, 43, 0);
  }

}

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

.banner-bg::after {
  content: '';
  position: absolute;
  width:100%;
  height:100%;
  max-height: 500px;
  background-color: rgba(0, 0, 0, 0.3);
  top:0;
  right: 0;
  z-index: 3;
  background: unset;
}


.banner-bg > picture {
  width:100%;
}

.banner-bg img {
  width:100%;
  height:100vh;
  max-height: 520px;
  object-fit: cover;
}

.banner-text {
  position: absolute;
  top:30%;
  left:22%;
  color:var(--brand-white);
  z-index: 5;
}

.banner-text .title {
  letter-spacing: 0.1rem;
  margin:0.5rem 0;
}

.banner-text .sub-title {
  letter-spacing: 0.05rem;
  margin:0.5rem 0;
}

@media (max-width:767.98px) {

  .banner-text {
    top:35%;
    left:0%;
  }

  .banner-text .sub-title {
    text-align: center;
  }

  .banner-text .title {
    text-align: center;
  }

}

section:after {
  content: '';
  position: absolute;
  width:100%;
  height:8px;
  background: linear-gradient(to right, #002f6c, #2cd5c4);
}

p {
  line-height: 1.5rem;
  text-align: center;
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
  color:var(--brand-white);
}

.banner .banner-text .title {
  letter-spacing: 0.1rem;
  margin:0.5rem 0;
}

.banner .banner-text .sub-title {
  letter-spacing: 0.05rem;
  margin:0.5rem 0;
}

@media (max-width:767.98px) {
  .banner .banner-text {
    top:10%;
    left:5%;
  }

}

.engineering .engineering-header {
  text-align: center;
  padding:2.5rem 0;
  margin:0;
  letter-spacing: 1px;
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
</style>
