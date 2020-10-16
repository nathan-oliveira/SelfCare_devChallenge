<template>
  <section class="itens">
    <div class="container">
      <div class="itens-left">
        <router-link to="/">PROMOÇÃO</router-link>
      </div>
      <nav class="itens-right">
        <ul>
          <li>
            <a href="">9 produtos</a>
          </li>
        </ul>
      </nav>
    </div>
  </section>
</template>

<script>
export default {
  name: "Nav",
  props: {
    msg: String,
  },
};
</script>

<style scoped lang="scss">
.container {
  align-items: center;
}

.itens {
  background: #ffffff;
  padding: 32px 10px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}

.itens-left {
  margin: 0 10px;
}

.itens-left a {
  font-size: 1.3rem;
  font-weight: 700;
  color: #161616;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  font-family: "Cabin", sans-serif;
}

.itens-right a {
  color: #161616;
  font-size: 1em;
}

.itens-right {
  flex: 1;
  margin: 0 10px;
  align-self: center;
}

.itens-right ul {
  float: right;
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

@media (max-width: 739px) {
  .itens {
    padding: 25px 0px;
  }
  .itens-right,
  .itens-left {
    margin: 0 20px;
  }
  .itens-left a {
    font-size: 1rem;
  }
  .itens-right a {
    font-size: 0.8rem;
  }
  .container {
    flex-direction: inherit !important;
  }
}
</style>
