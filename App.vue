<script setup>
import { ref } from 'vue'

const name = ref('')
const password = ref('')
const repassword = ref('')
const date = ref(0)
const adress = ref('')
const city = ref('')
const state = ref('')
const hobbies = ref('')
const bio = ref('')
const enviar = ref(false)

</script>

<template>
  <div class="container">
    <div class="info">
      <form action="" @submit.prevent="">
        <h1>Formulario DESWEB</h1>
        <hr>
        <p>name:</p>
        <input type="text" v-model="name" placeholder="Nome" required />
        <p>Senha:</p>
        <input type="password" v-model="password" placeholder="Senha" required />
        <p>Confirmar password:</p>
        <input type="password" v-model="repassword" placeholder="Confirmar senha" required />
        <p>date de nascimento:</p>
        <input type="date" v-model="date" placeholder="Data de Nascimento" required />
        <p>Endereço:</p>
        <input type="text" v-model="adress" placeholder="Endereço" required />
        <p>city:</p>
        <input type="text" v-model="city" placeholder="cidade" required />
        <p>seu estado:</p>
        <select v-model="state" placeholder="AC">
          <option value="AC">AC</option>
          <option value="AL">AL</option>
          <option value="AP">AP</option>
          <option value="AM">AM</option>
          <option value="BA">BA</option>
          <option value="CE">CE</option>
          <option value="DF">DF</option>
          <option value="ES">ES</option>
          <option value="GO">GO</option>
          <option value="MA">MA</option>
          <option value="MT">MT</option>
          <option value="MS">MS</option>
          <option value="MG">MG</option>
          <option value="PA">PA</option>
          <option value="PB">PB</option>
          <option value="PR">PR</option>
          <option value="PE">PE</option>
          <option value="PI">PI</option>
          <option value="RJ">RJ</option>
          <option value="RN">RN</option>
          <option value="RS">RS</option>
          <option value="RO">RO</option>
          <option value="RR">RR</option>
          <option value="SC">SC</option>
          <option value="SP">SP</option>
          <option value="SE">SE</option>
          <option value="TO">TO</option>
        </select>
        <p style="white-space: pre-line;">Hobbies</p>
        <textarea v-model="hobbies" />
  
        <p style="white-space: pre-line;">bio:</p>
        <textarea v-model="bio" />
        <hr>
        <button type="submit" @click="enviar = !enviar">Salvar informações</button>

      </form>

    </div>
    <!-- div .container -->
  </div>

  <div class="container">
    <div v-if="enviar" class="info">
      <h1>Informações Salvas</h1>
      <hr>
      <div class="margemTexto">
        Nome: {{ name }}
      </div>
      <div class="margemTexto">
        Senha: {{ password }}
      </div>
      <div class="margemTexto">
        Confirmar Senha: {{ repassword }}
      </div>
      <div class="margemTexto">
        Data de Nascimento: {{ date }}
      </div>
      <div class="margemTexto">
        Endereço: {{ adress }}
      </div>
      <div class="margemTexto">
        Cidade: {{ city }}
      </div>
      <div class="margemTexto">
        Hobbies: {{ hobbies }}
      </div>
    
      <div class="margemTexto">
        bio: {{ bio }}
      </div>
    </div>
  </div>
  <div>
    <p>BY EDUARDUUOLIVEIRA</p>
  </div>
</template>

<style scoped>
.container {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20px;
}

button {
  font-weight: bold;
  margin: 0 20px;
  background-color: black;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 15px 20px;
  cursor: pointer;
}

.info {
  background-color: rgba(44, 6, 209, 0.938);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  text-align: center;
  margin: 10px;
  width: 44%;
}

.border-radius {
  border-radius: 15px;
}

p {
  margin: 50px 50px 50px 50px;

}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}

p {
  margin: 15px 15px 15px 15px;
}

.margemTexto {
  margin: 15px 15px 15px 15px;
}

.radioCss {
  margin-left: 15px;
}
</style>
