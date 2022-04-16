<template>

  <section>
    <div class="no-page-wrapper">
      <img src="@/assets/images/404.webp" alt="404">
      <h2>
        <span>404</span><br>
        Такой страницы не существует ;(
      </h2>
    </div>
  </section>

</template>

<style scoped>
.no-page-wrapper {
  width:100%;
  display: flex;
  align-content: center;
  align-items: center;
  justify-content: center;
  text-align: center;
  font-size:2rem;
  height:calc(100vh - 400px);
  padding:2rem 0;
}

.no-page-wrapper > img {
  width:100%;
  max-width:200px;
}
.no-page-wrapper > h2 {
  margin:0;
  line-height: 4.5rem;
}

.no-page-wrapper > h2 > span {
  color:#002f6c;
  font-size: 5rem;
}
</style>
