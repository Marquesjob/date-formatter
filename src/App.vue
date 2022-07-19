<script >
</script>
<template>


  <div class="infos">
    <div class="title">Date Formatter</div>
    <div class="description">
      <p>Pequeno projeto prático criado para estudo, que tem a finalidade de praticar<br /> o processo de recepção e
        formatação de datas recebidas de uma <strong>API</strong> Utilizando<strong> Javascript.</strong></p>
      <p><strong>API</strong> utilizada no projeto:<a href="https://jsonplaceholder.typicode.com/"
          target="__blank">  JSONPlaceholder — Free Fake REST API.</a></p>
    </div>
  </div>

  <div class="content">

    <div class="container__received">
      <label for="receveidData"> — Data Recebida — </label>
      <input id="receveidData" type="text">
    </div>

    <div class="container__converted">
      <label for="convertedData"> — Data Convertida — </label>
      <input id="convertedData" type="text">
    </div>

  </div>

</template>

<style >
.infos {
  width: 55%;
  margin: 0 auto;
  border-bottom: 1px solid var(--vt-c-green);
  margin-bottom: 20px;
}

.description {
  margin-bottom: 15px;
}

.title {
  font-size: 30px;
  color: var(--vt-c-green);
  display: flex;
  justify-content: center;
}

p {
  text-align: center;
}

a {
  font-style: italic;
  font-weight: lighter;
}

strong {
  font-weight: bold;
  color: rgb(182, 184, 192);
}

.content {
  width: 55%;
  height: 600px;
  margin: 0 auto;
}

input {
  width: 300px;
  height: 30px;
  display: block;
  margin: 0 auto;
  border: none;
  background-color: rgb(65, 65, 65);
  padding: 5px;
  color: rgb(190, 190, 190);
  font-style: italic;
}

input:active, input:focus {
  outline: none;
}

label {
  width: fit-content;
  height: fit-content;
  display: block;
  margin: 0 auto;
  margin-bottom: 5px;
  color: rgb(221, 221, 221);
}

.container__converted {
  margin-top: 10px;
}
</style>
