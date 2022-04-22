<template>
  <article>
    <form action="" method="post" @submit="onSubmit">
      <div class="form-block name">
        <label for="name">Имя</label>
        <input v-model="name" type="text" id="name" name="user_name" placeholder="Введите ваше имя" />
      </div>
      <div class="form-block phone">
        <label for="phone">Ваш телефон:</label>
        <input v-model="phone" type="phone" id="phone" name="user_phone" placeholder="+7(___)___-__-__"/>
      </div>
      <input type="submit" value="Заказать звонок"><br>
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
      phone: ''
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
      console.log(jsonData)

    }
  }
}
</script>

<style scoped>
form {
  margin:2rem auto;
  display: flex;
  justify-content: center;
  flex-direction: column;
  width:100%;
  max-width:620px;
  height:400px;
  border: 3px solid var(--brand-blue);
  padding:2rem;
}

form .form-block {
  display: flex;
  flex-direction: column;
  margin-bottom: 1.5rem;
}

form .form-block > input {
  width:100%;
  padding:0.5rem;
}

form .form-block > input:focus {
  outline: none;
}


form .form-block > label {
  margin-bottom: 0.25rem;
}

form .accept {
  font-size:0.7rem;
  color: var(--brand-black);
}

form .accept .special {
  color:var(--brand-blue);
  font-weight: bold;
}
</style>
