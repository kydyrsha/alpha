<template>
  <section>
    <div class="container">
      <div class="contacts-wrapper">
        <div class="contacts">
          <h2>Контакты:</h2>
          <p>Республика Казахстан, город Алматы, Зеина Шашкина, 9Б</p>
          <div class="navbar-links">
            <a class="phone" href="tel:+77273270087">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="20" height="20"><path fill="none" d="M0 0h24v24H0z"/><path d="M21 16.42v3.536a1 1 0 0 1-.93.998c-.437.03-.794.046-1.07.046-8.837 0-16-7.163-16-16 0-.276.015-.633.046-1.07A1 1 0 0 1 4.044 3H7.58a.5.5 0 0 1 .498.45c.023.23.044.413.064.552A13.901 13.901 0 0 0 9.35 8.003c.095.2.033.439-.147.567l-2.158 1.542a13.047 13.047 0 0 0 6.844 6.844l1.54-2.154a.462.462 0 0 1 .573-.149 13.901 13.901 0 0 0 4 1.205c.139.02.322.042.55.064a.5.5 0 0 1 .449.498z" fill="rgba(0,47,108,1)"/></svg>
              +7-727-327-00-87
            </a>
            <a href="https://api.whatsapp.com/send/?phone=87058073742&text=Здравствуйте!" class="whatsapp">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M7.253 18.494l.724.423A7.953 7.953 0 0 0 12 20a8 8 0 1 0-8-8c0 1.436.377 2.813 1.084 4.024l.422.724-.653 2.401 2.4-.655zM2.004 22l1.352-4.968A9.954 9.954 0 0 1 2 12C2 6.477 6.477 2 12 2s10 4.477 10 10-4.477 10-10 10a9.954 9.954 0 0 1-5.03-1.355L2.004 22zM8.391 7.308c.134-.01.269-.01.403-.004.054.004.108.01.162.016.159.018.334.115.393.249.298.676.588 1.357.868 2.04.062.152.025.347-.093.537a4.38 4.38 0 0 1-.263.372c-.113.145-.356.411-.356.411s-.099.118-.061.265c.014.056.06.137.102.205l.059.095c.256.427.6.86 1.02 1.268.12.116.237.235.363.346.468.413.998.75 1.57 1l.005.002c.085.037.128.057.252.11.062.026.126.049.191.066a.35.35 0 0 0 .367-.13c.724-.877.79-.934.796-.934v.002a.482.482 0 0 1 .378-.127c.06.004.121.015.177.04.531.243 1.4.622 1.4.622l.582.261c.098.047.187.158.19.265.004.067.01.175-.013.373-.032.259-.11.57-.188.733a1.155 1.155 0 0 1-.21.302 2.378 2.378 0 0 1-.33.288 3.71 3.71 0 0 1-.125.09 5.024 5.024 0 0 1-.383.22 1.99 1.99 0 0 1-.833.23c-.185.01-.37.024-.556.014-.008 0-.568-.087-.568-.087a9.448 9.448 0 0 1-3.84-2.046c-.226-.199-.435-.413-.649-.626-.89-.885-1.562-1.84-1.97-2.742A3.47 3.47 0 0 1 6.9 9.62a2.729 2.729 0 0 1 .564-1.68c.073-.094.142-.192.261-.305.127-.12.207-.184.294-.228a.961.961 0 0 1 .371-.1z" fill="rgba(0,47,108,1)"/></svg>
              +7-705-807-37-42
            </a>
            <a class="email" href="mailto:info@alphamet.kz">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="20" height="20"><path fill="none" d="M0 0h24v24H0z"/><path d="M3 3h18a1 1 0 0 1 1 1v16a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1zm17 4.238l-7.928 7.1L4 7.216V19h16V7.238zM4.511 5l7.55 6.662L19.502 5H4.511z" fill="rgba(0,47,108,1)"/></svg>
              info@alphamet.kz
            </a>
          </div>
        </div>
        <div class="map-wrapper">
          <h2 style="opacity:0;">Как к нам добраться?</h2>
          <div id="map" style="width:800px; height:600px"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
var map;

DG.then(function () {
  map = DG.map('map', {
    center: [76.93, 43.22],
    zoom: 13
  });
  // DG.marker([76.93, 43.22]).addTo(map);
});
</script>
<style scoped>
h2 {
  line-height: 2rem;
  font-size: 2.5rem;
  font-weight: normal;
}

p {
  line-height: 1.75rem;
  font-size: 1.25rem;
}

.navbar-links > a {
  text-decoration: none;
  color: #000;
  display: flex;
  flex-direction: row;
  align-items: center;
  transition: 0.6s;
  margin-bottom: 1rem;
}

.navbar-links > a:hover {
  opacity: 0.7;
}

.navbar-links > a > svg {
  margin-right: 0.5rem;
}

.contacts-wrapper {
  display:flex;
}

.contacts-wrapper .map-wrapper {
  width:70%;
}

.contacts-wrapper .map-wrapper #map {
  margin-bottom: 1rem;
}

.contacts-wrapper .contacts {
  width:30%;
}

/*.container {*/
/*  height:calc(100vh - 54px);*/
/*}*/

@media (max-width:767.98px) {
  .contacts-wrapper {
    flex-direction: column;
  }

  .contacts-wrapper .contacts {
    width:100%;
  }

  .contacts-wrapper .map-wrapper {
    width:100%;
  }

  .contacts-wrapper .map-wrapper > h2 {
    display:none;
  }

  .contacts-wrapper .map-wrapper #map {
    width:100% !important;
  }

}
</style>