<template>
  <article class="form-wrapper">
    <form action="" method="post" @submit="onSubmit">
      <span class="close-form" @click="toggleForm()"><img src="@/assets/images/close.png" alt="close-icon" title="close icon"/></span>
      <div class="form-block name">
        <label for="name">Имя:</label>
        <input v-model="name" type="text" id="name" name="user_name" placeholder="Введите ваше имя" />
      </div>
      <div class="form-block phone">
        <label for="phone">Ваш телефон:</label>
        <input v-maska="['+7 (###) ##-##-##', '+7 (###) ###-##-##']" v-model="phone" type="phone" id="phone" name="user_phone" placeholder="+7(___)___-__-__" >
      </div>
      <input class="order-call" type="submit" value="Заказать звонок">
      <a class="accept" href="#">Нажимая кнопку “Заказать звонок”, вы принимаете <RouterLink class="special" to="/docs">условия обработки персональных данных</RouterLink></a>
    </form>
  </article>
</template>

<script>
export default {
  name : 'Form',
  data: () => {
    return {
      name: '',
      phone: '',
      isShow: false
    }
  },
  methods: {
    async onSubmit(event) {
      event.preventDefault()
      let response = await fetch('https://alphamet.kz/sendMail.php', {
        method: 'POST',
        body: JSON.stringify({
          name: this.name,
          phone: this.phone
        })
      })
      let jsonData = await response.json()
      // console.log(jsonData)
    }
  }
}
</script>

<style scoped>

.form-wrapper {
  background: rgba(0,0,0,0.6);
  position: fixed;
  width: 100%;
  height: 100vh;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 100;
  display:none;
}

.form-wrapper form {
  margin:2rem auto;
  display: flex;
  justify-content: center;
  flex-direction: column;
  width:100%;
  max-width:500px;
  height:400px;
  border: 3px solid var(--brand-blue);
  padding:4rem;
  background-color: var(--pure-white);
  position: relative;
}

.form-wrapper form .close-form {
  position: absolute;
  right:2%;
  top:3%;
}

.form-wrapper form .close-form > img {
  width:25px;
  cursor: pointer;
}

.form-wrapper form .form-block {
  display: flex;
  flex-direction: column;
  margin-bottom: 1.5rem;
}

.form-wrapper form .form-block.phone {
  margin-bottom: 2.5rem;
}

.form-wrapper form .form-block > input {
  width:100%;
  padding:0.75rem;
  border:0.5px solid var(--brand-blue);
  -webkit-transition: all 0.3s ease-in-out;
  -moz-transition: all 0.3s ease-in-out;
  -ms-transition: all 0.3s ease-in-out;
  -o-transition: all 0.3s ease-in-out;
}

.form-wrapper form .form-block > input::placeholder {
  color:var(--brand-black);
  font-family: inherit;
}

.form-wrapper form .form-block > input:focus {
  outline: none;
  box-shadow: 0 0 5px rgba(0, 71, 177, 1);
  /*border: none;*/
}

.form-wrapper form .form-block > label {
  margin-bottom: 0.5rem;
  /*font-weight: 600;*/
}

.form-wrapper form .accept {
  font-size:0.7rem;
  color: var(--brand-black);
}

.form-wrapper form .accept .special {
  color:var(--brand-blue);
  font-weight: bold;
}

.form-wrapper form .order-call {
  cursor: pointer;
  color: var(--brand-blue);
  background-color: var(--brand-blue);
  border:1px solid var(--pure-white);
  color:var(--pure-white);
  padding:0.75rem 0.5rem;
  margin-bottom: 0.5rem;
  transition: 0.6s;
}

.form-wrapper form .order-call:hover {
  background-color: var(--brand-white);
  border:1px solid var(--brand-blue);
  color: var(--brand-blue);
}
</style>
