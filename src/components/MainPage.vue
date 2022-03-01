<template>
  <section class="banner">
    <div class="banner-bg">
      <video class="alphamet-intro" autoplay loop muted playsinline>
        <source src="@/assets/video/alphamet.mp4" type="video/mp4" />
      </video>
    </div>
    <div class="banner-text">
      <h1 class="title">Компания Alphamet</h1>
      <h2 class="sub-title">Комплексные решения для нефтехимической<Br/>и горнодобывающей отрасли</h2>
    </div>
  </section>
  <section class="engineering">
    <div class="container">
      <h2 class="engineering-header">Проектирование</h2>
      <div class="engineering-wrapper">
        <div class="engineering-block">
          <img src="@/assets/images/engineering/block1.png" alt="factory-icon">
          <p>Проектирование (технологическое) нефтехимических производств</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/engineering/block2.png" alt="paper-icon">
          <p>Cоставление проектных документов для месторождений углеводородного сырья</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/engineering/block3.png" alt="paper-icon">
          <p>Составление технико-экономического обоснования проектов для месторождений углеводородного сырья</p>
        </div>
        <div class="engineering-block">
          <img src="@/assets/images/engineering/block4.png" alt="factory-icon">
          <p>Составление технологических регламентов для месторождений углеводородного сырья</p>
        </div>
      </div>
    </div>
  </section>
  <section class="supply">
    <div class="container">
      <div class="supply-wrapper">
        <h2 class="supply-header">
          Поставка материалов и оборудования
        </h2>
        <p class="supply-text">Компания «Alphamet» осуществляет поставку широкого спектра материалов и оборудования для нефтегазовой и горнодобывающей отрасли, изготовление и поставка нефтяных труб (обсадные, бурильные, НТК и другие), комплектующие детали и расходные материалы для строительства и ремонта технологических трубопроводов, конструкции для строительства переходов через преграды, изделия из полимеров и полиуретанов, металлоконструкции и другие детали трубопровода, необходимые для обустройства месторождений и строительства резервуарных парков. С основными каталогами продукции предлагаем ознакомиться в разделе продукция.</p>
      </div>
    </div>
  </section>
</template>


<style scoped>

h2 {
  font-weight: normal;
  font-size: 2rem;
}

p {
  line-height: 1.5rem;
  text-align: justify;
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
}

@media (max-width:767.98px) {
  .banner .alphamet-intro {
    min-height: 500px;
  }
  .banner .banner-text {
    top:10%;
    left:7%;
  }

}

.engineering .engineering-header {
  text-align: center;
  font-size: 2rem;
  margin:2.5rem 0;
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
  width:45%;
  display:flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 1.5rem;
}

.engineering .engineering-wrapper .engineering-block > img {
  width:15%;
}

.engineering .engineering-wrapper .engineering-block > p {
  width:80%;
}


.engineering .engineering-wrapper:after {
  content: '';
  position: absolute;
  width:40%;
  height: 3px;
  background-color:#33337b;
  bottom:0;
}

@media (max-width: 767.98px) {
  .engineering .engineering-wrapper {
    flex-direction: column;
  }

  .engineering .engineering-wrapper .engineering-block {
    width:100%;
  }

  .engineering .engineering-wrapper .engineering-block > img {
    width:20%;
  }

  .engineering .engineering-wrapper .engineering-block > p {
    width:75%;
  }
}

.supply .supply-wrapper {
  position: relative;
  padding-bottom: 2rem;
}

/*.supply .supply-wrapper:after {*/
/*  content: '';*/
/*  position: absolute;*/
/*  width:40%;*/
/*  height: 3px;*/
/*  background-color:#33337b;*/
/*  bottom:0;*/
/*  right:0;*/
/*}*/

.supply .supply-header {
  text-align: center;
  margin-top: 2rem;
}

.supply .supply-text {
  line-height: 1.5rem;
  text-align: justify;
}


</style>
