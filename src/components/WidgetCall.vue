<template>
  <div class="widget-wrapper">
    <a class="widget-call" href="#" @click="toggleForm()"><img class="active" src="@/assets/images/ringing.png" alt="phone-icon" title="call"></a>
  </div>
</template>

<script>
// export default {
//   methods: {
//     toggleForm() {
//       event.preventDefault()
//       this.isShow = !this.isShow
//     }
//   }
// }
</script>

<style scoped>
.widget-call {
  position: fixed;
  right: 3%;
  bottom: 5%;
  z-index: 100;
}

@media (max-width:767.98px) {
  .widget-call {
    right:6%;
    bottom:2%;
  }

  .widget-call > img {
    max-width:80px;
  }
}

.widget-call > img {
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

</style>
