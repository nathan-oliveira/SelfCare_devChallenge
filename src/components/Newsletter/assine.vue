<template>
  <section class="assine">
    <div class="container">
      <div class="assine-info">
        <p>Contato</p>
        <p>Termos de seviços</p>
        <p>Política de privacidade</p>
        <p>Cancelamento, troca e reembolso</p>
      </div>
      <form>
        <label>Newsletter</label>
        <input type="text" placeholder="Digite seu melhor e-mail" />
        <button type="submit">Inscrever</button>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  name: "assine",
};
</script>

<style lang="scss" scoped>
.assine {
  background: #f9f9f9;
  padding: 40px 10px;
  margin-top: 100px;
  border-top: 1px solid rgba(0, 0, 0, 0.1);
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}

.assine-info {
  flex: 1;
  margin: 0 10px;
}

.assine-info p {
  font-size: 1.25rem;
  margin-bottom: 11px;
}

.assine form {
  flex: 1;
  margin: 0 10px;
  display: flex;
  flex-wrap: wrap;
  align-content: flex-start;
}

.assine form label {
  width: 100%;
  margin-top: 10px;
  margin-bottom: 15px;
  font-weight: 500;
  font-size: 1.25rem;
}

.assine input {
  flex: 1;
  align-self: flex-start;
  padding: 15px;
  border: 1px solid rgba(0, 0, 0, 0.1);
  background: none;
  font-size: 1em;
  font-family: "Lato", Georgia, serif;
  outline: none;
  border-radius: 5px 0px 0px 5px;
}

.assine button {
  align-self: flex-start;
  padding: 16px 40px;
  background: #5ca720;
  border-radius: 0px 5px 5px 0px;
  border: none;
  font-family: "Lato", Georgia, serif;
  font-weight: 700;
  font-size: 1em;
  color: #fff;
  outline: none;
  cursor: pointer;
}

@media (min-width: 740px) {
  .assine form {
    margin-left: 200px;
  }
}

@media (max-width: 739px) {
  .assine {
    padding: 40px 20px;
  }
  .assine-info {
    margin: 0 0 20px 0;
  }

  .assine {
    margin-top: 40px;
  }

  .assine form {
    margin: 0px;
  }

  .assine-info p,
  .assine form label {
    font-size: 1rem;
  }
}

@media (max-width: 391px) {
  .assine button,
  .assine input {
    width: 100%;
    border-radius: 5px;
  }

  .assine button {
    margin-top: 4%;
  }
}
</style>
