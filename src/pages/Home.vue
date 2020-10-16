<template>
  <div class="content">
    <NavBar />
    <Main />
    <MainNav />
    <Carrinho />
    <Assine />
    <Rodape />
  </div>
</template>

<script>
import NavBar from "@/components/Nav/NavBar.vue";
import Main from "@/components/Main/Main.vue";
import MainNav from "@/components/Main/Nav.vue";
import Carrinho from "@/components/Cart/Carrinho.vue";
import Assine from "@/components/Newsletter/assine.vue";
import Rodape from "@/components/Footer/rodape.vue";

export default {
  name: "Home",
  components: {
    Main,
    MainNav,
    Carrinho,
    Assine,
    Rodape,
    NavBar,
  },
};
</script>
