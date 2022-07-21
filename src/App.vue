<script >
import TimeLine from "./components/timeLine.vue";

export default {
    data() {
        return {
            response: [],
            receivedDate: new Date,
            convertedDate: ""
        };
    },
    mounted() {
        fetch("https://jsonplaceholder.typicode.com/posts", {
            method: "POST",
            body: JSON.stringify({
                date: new Date,
            }),
            headers: {
                "Content-type": "application/json; charset=UTF-8",
            },
        })
            .then((response) => response.json())
            .then((json) => {
            this.response = json;
        });
    },
    components: { TimeLine }
}

</script>
<template>


  <div class="infos">
    <div class="title">Date Formatter</div>
    <div class="description">
      <p>Pequeno projeto criado para estudo, que tem a finalidade de praticar o processo de recepção e<br />
        formatação de datas recebidas no formato <strong>UTC</strong> de uma <strong>API</strong> Utilizando<strong>
          Javascript.</strong></p>
      <p><strong>API</strong> utilizada no projeto<strong>:</strong><a href="https://jsonplaceholder.typicode.com/"
          target="__blank"> JSONPlaceholder — Free Fake REST API.</a></p>
    </div>
  </div>

  <div class="content">

    <div class="container__received">
      <label for="receveidData"> — Data Recebida — </label>
      <input id="receveidData" type="text" v-bind:value="response.date" disabled>
    </div>

    <div class="container__converted">
      <label for="convertedData"> — Data Convertida — </label>
      <input id="convertedData" type="text" v-bind:value="response.date" disabled>
    </div>

    <div class="container__button">
      <button id="format">Formatar</button>
    </div>

  </div>

  <TimeLine />

</template>

<style >

.infos {
  padding-bottom: 25px;
  width: 55%;
  margin: 0 auto;
  border-bottom: 1px solid var(--vt-c-green);
  margin-bottom: 40px;
}

.description {
  margin-bottom: 15px;
}

.title {
  margin-bottom: 15px;
  font-size: 30px;
  color: var(--vt-c-green);
  display: flex;
  justify-content: center;
}

p {
  text-align: center;
}

a {
  margin-left: 3px;
  font-style: italic;
  font-weight: lighter;
}

strong {
  font-weight: bold;
  color: rgb(182, 184, 192);
}

.content {
  width: 55%;
  height: auto;
  margin: 0 auto;
  margin-bottom: 40px;
  border-bottom: 1px solid var(--vt-c-green);
}

input {
  width: 300px;
  height: 35px;
  display: block;
  margin: 0 auto;
  border: none;
  background-color: rgb(65, 65, 65);
  padding: 5px;
  color: rgb(190, 190, 190);
  font-style: italic;
}

input:active,
input:focus {
  outline: none;
}

#receveidData, #convertedData{
  text-align: center;
}

label {
  width: fit-content;
  height: fit-content;
  display: block;
  margin: 0 auto;
  margin-bottom: 12px;
  color: rgb(221, 221, 221);
}

.container__converted {
  margin-top: 15px;
}

.container__button {
  display: flex;
  justify-content: center;
  margin-top: 20px;
  width: 100%;
  height: fit-content;
}

#format,
button {
  margin-top: 8px;
  margin-bottom: 40px;
  height: 38px;
  color: black;
  background-color: var(--vt-c-black);
  outline: none;
  border: none;
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
  width: 300px;
  font-size: 15px;
  border-radius: 5px;
}

#format:hover {
  background-color: hsla(160, 100%, 37%, 0.2);
}
</style>
