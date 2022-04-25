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
          <img src="@/assets/images/services/sketch.png" alt="sketch-icon" title="sketch icon"/>
          <p>Проектирование (технологическое)<br>нефтехимических производств</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/services/block3.png" alt="paper-icon" title="paper icon"/>
          <p>Составление технико-экономического<br>обоснования проектов</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/services/tubes.png" alt="pipe-icon" title="pipe icon"/>
          <p>Поставка труб различных<br>диаметров и марок стали</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/services/laboratory.png" alt="lab-icon" title="lab icon"/>
          <p>Поставка промышленного<br>и технического оборудования</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/services/corrosive.png" alt="corrosive-icon" title="corrosive icon"/>
          <p>Антикоррозийное<br>покрытие</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/services/maintenance.png" alt="lab-icon" title="lab icon"/>
          <p>Строительно-монтажные<br>работы</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// export default {
//   data() {
//     return {
//       isShow: false
//     }
//   },
//   methods: {
//     openForm() {
//       console.log(212121)
//       event.preventDefault()
//       this.isShow = !this.isShow
//       console.log(this.isShow)
//     }
//   }
// }
</script>


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
  display: flex;
}

.banner-bg img {
  width:100%;
  height:100vh;
  max-height: 520px;
  object-fit: cover;
  transition: 0.6s;
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
  text-align: center;
}

.banner-bg::after {
  content: '';
  position: absolute;
  width:100%;
  height:100%;
  max-height: 520px;
  background-color: rgba(0, 0, 0, 0.5);
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
  margin:0;
  letter-spacing: 1px;
  padding:2rem 0;
}

.engineering .engineering-wrapper {
  display:flex;
  justify-content: space-between;
  flex-wrap: wrap;
  position: relative;
  padding-bottom: 2rem;
}

.engineering .engineering-wrapper .engineering-block {
  width:50%;
  display:flex;
  align-items: center;
  transition: 0.6s;
  padding:1rem;
}

.engineering .engineering-wrapper .engineering-block:hover {
  -webkit-box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.4);
  -moz-box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.4);
  box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.4);
}

.engineering .engineering-wrapper .engineering-block > img {
  width:17%;
  padding:0.25rem;
}

.engineering .engineering-wrapper .engineering-block > p {
  width:80%;
  margin:0;
}

@media (max-width: 911.98px) {
  .engineering .engineering-wrapper {
    flex-direction: column;
  }

  .engineering .engineering-wrapper .engineering-block {
    width:100%;
    margin-bottom: 2rem;
    justify-content: center;
  }

  .engineering .engineering-wrapper .engineering-block > img {
    width:20%;
  }

  .engineering .engineering-wrapper .engineering-block > p {
    width:75%;
  }
}
</style>
