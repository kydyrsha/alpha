<template>
  <footer>
    <div class="container">
      <div class="footer-wrapper">
        <RouterLink class="logo-link" to="/"><img class="footer-logo" src="@/assets/images/alphamet-transparent.png"
                                                  alt="logo" title="Alphamet logo"></RouterLink>
        <div class="docs">
          <h2 class="footer-title">Документы:</h2>
          <RouterLink class="footer-link" to="/docs">Согласие на сбор и обработку персональных данных</RouterLink>
        </div>
        <div class="socials">
          <h2 class="footer-title">Мы в социальных сетях:</h2>
          <a href="https://www.instagram.com/alphamet.kz/" class="footer-link social-link"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M12 9a3 3 0 1 0 0 6 3 3 0 0 0 0-6zm0-2a5 5 0 1 1 0 10 5 5 0 0 1 0-10zm6.5-.25a1.25 1.25 0 0 1-2.5 0 1.25 1.25 0 0 1 2.5 0zM12 4c-2.474 0-2.878.007-4.029.058-.784.037-1.31.142-1.798.332-.434.168-.747.369-1.08.703a2.89 2.89 0 0 0-.704 1.08c-.19.49-.295 1.015-.331 1.798C4.006 9.075 4 9.461 4 12c0 2.474.007 2.878.058 4.029.037.783.142 1.31.331 1.797.17.435.37.748.702 1.08.337.336.65.537 1.08.703.494.191 1.02.297 1.8.333C9.075 19.994 9.461 20 12 20c2.474 0 2.878-.007 4.029-.058.782-.037 1.309-.142 1.797-.331.433-.169.748-.37 1.08-.702.337-.337.538-.65.704-1.08.19-.493.296-1.02.332-1.8.052-1.104.058-1.49.058-4.029 0-2.474-.007-2.878-.058-4.029-.037-.782-.142-1.31-.332-1.798a2.911 2.911 0 0 0-.703-1.08 2.884 2.884 0 0 0-1.08-.704c-.49-.19-1.016-.295-1.798-.331C14.925 4.006 14.539 4 12 4zm0-2c2.717 0 3.056.01 4.122.06 1.065.05 1.79.217 2.428.465.66.254 1.216.598 1.772 1.153a4.908 4.908 0 0 1 1.153 1.772c.247.637.415 1.363.465 2.428.047 1.066.06 1.405.06 4.122 0 2.717-.01 3.056-.06 4.122-.05 1.065-.218 1.79-.465 2.428a4.883 4.883 0 0 1-1.153 1.772 4.915 4.915 0 0 1-1.772 1.153c-.637.247-1.363.415-2.428.465-1.066.047-1.405.06-4.122.06-2.717 0-3.056-.01-4.122-.06-1.065-.05-1.79-.218-2.428-.465a4.89 4.89 0 0 1-1.772-1.153 4.904 4.904 0 0 1-1.153-1.772c-.248-.637-.415-1.363-.465-2.428C2.013 15.056 2 14.717 2 12c0-2.717.01-3.056.06-4.122.05-1.066.217-1.79.465-2.428a4.88 4.88 0 0 1 1.153-1.772A4.897 4.897 0 0 1 5.45 2.525c.638-.248 1.362-.415 2.428-.465C8.944 2.013 9.283 2 12 2z" fill="rgba(246,245,250,1)"/></svg></a>
          <a href="https://www.facebook.com/profile.php?id=100080152398704" class="footer-link social-link"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M12 2C6.477 2 2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.879V14.89h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.989C18.343 21.129 22 16.99 22 12c0-5.523-4.477-10-10-10z" fill="rgba(246,245,250,1)"/></svg></a>
        </div>
        <div class="contacts">
          <h2 class="footer-title">Связаться с нами:</h2>
          <a href="mailto:info@alphamet.kz" class="footer-link contact-link"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M22 20.007a1 1 0 0 1-.992.993H2.992A.993.993 0 0 1 2 20.007V19h18V7.3l-8 7.2-10-9V4a1 1 0 0 1 1-1h18a1 1 0 0 1 1 1v16.007zM4.434 5L12 11.81 19.566 5H4.434zM0 15h8v2H0v-2zm0-5h5v2H0v-2z" fill="rgba(246,245,250,1)"/></svg></a>
          <a href="https://api.whatsapp.com/send/?phone=87006055555&text=Здравствуйте!%20Пишу по поводу вашей продукции" class="footer-link contact-link"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M7.253 18.494l.724.423A7.953 7.953 0 0 0 12 20a8 8 0 1 0-8-8c0 1.436.377 2.813 1.084 4.024l.422.724-.653 2.401 2.4-.655zM2.004 22l1.352-4.968A9.954 9.954 0 0 1 2 12C2 6.477 6.477 2 12 2s10 4.477 10 10-4.477 10-10 10a9.954 9.954 0 0 1-5.03-1.355L2.004 22zM8.391 7.308c.134-.01.269-.01.403-.004.054.004.108.01.162.016.159.018.334.115.393.249.298.676.588 1.357.868 2.04.062.152.025.347-.093.537a4.38 4.38 0 0 1-.263.372c-.113.145-.356.411-.356.411s-.099.118-.061.265c.014.056.06.137.102.205l.059.095c.256.427.6.86 1.02 1.268.12.116.237.235.363.346.468.413.998.75 1.57 1l.005.002c.085.037.128.057.252.11.062.026.126.049.191.066a.35.35 0 0 0 .367-.13c.724-.877.79-.934.796-.934v.002a.482.482 0 0 1 .378-.127c.06.004.121.015.177.04.531.243 1.4.622 1.4.622l.582.261c.098.047.187.158.19.265.004.067.01.175-.013.373-.032.259-.11.57-.188.733a1.155 1.155 0 0 1-.21.302 2.378 2.378 0 0 1-.33.288 3.71 3.71 0 0 1-.125.09 5.024 5.024 0 0 1-.383.22 1.99 1.99 0 0 1-.833.23c-.185.01-.37.024-.556.014-.008 0-.568-.087-.568-.087a9.448 9.448 0 0 1-3.84-2.046c-.226-.199-.435-.413-.649-.626-.89-.885-1.562-1.84-1.97-2.742A3.47 3.47 0 0 1 6.9 9.62a2.729 2.729 0 0 1 .564-1.68c.073-.094.142-.192.261-.305.127-.12.207-.184.294-.228a.961.961 0 0 1 .371-.1z" fill="rgba(246,245,250,1)"/></svg></a>
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
  background: var(--brand-blue);
}

footer .footer-wrapper {
  padding:1.5rem 0;
  display: flex;
  align-items: flex-start;
}

footer .footer-wrapper .docs .footer-link {
  width:100%;
  text-align: center;
}

footer .footer-wrapper > * {
  width:25%;
}

footer .footer-logo {
  width:100%;
  max-width:200px;
}

.footer-wrapper .footer-title {
  color: var(--brand-white);
  margin:0;
  font-size:1.25rem;
  padding-bottom: 1rem;
  text-align: center;
}

.footer-wrapper .footer-link {
  color: var(--brand-white);
  transition: 0.6s;
  width:50%;
  display: inline-block;
  text-align: center;
}

.footer-wrapper .footer-link:hover {
  opacity:0.8;
}

.footer-wrapper .footer-link > svg {
  transition: 0.6s;
}

.footer-wrapper .footer-link:hover > svg {
  opacity:0.8;
}

@media (max-width:767.98px) {
  footer .footer-wrapper {
    flex-direction: column;
  }

  footer .footer-wrapper > * {
    width:100%;
  }

  footer .footer-wrapper > *:not(:last-child) {
    margin-bottom: 2rem;
  }

  footer .logo-link {
    text-align: center;
  }

  .footer-wrapper .footer-title {
    text-align: center;
  }

  footer .footer-wrapper .docs .footer-link {
    text-align: center;
    max-width: 80%;
    display: block;
    margin: 0 auto;
  }

}
</style>
