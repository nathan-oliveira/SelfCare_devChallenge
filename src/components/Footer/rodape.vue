<template>
  <footer class="footer animate" data-anime="top">
    <div class="container footer-row">
      <div class="footer-social">
        <Instagram />
        <Facebook />
      </div>
      <div class="footer-card">
        <MasterCard />
        <PayPal />
        <Visa />
      </div>
    </div>
  </footer>
</template>

<script>
import MasterCard from "@/components/svg/mastercard.vue";
import Instagram from "@/components/svg/instagram.vue";
import Facebook from "@/components/svg/facebook.vue";
import PayPal from "@/components/svg/paypal.vue";
import Visa from "@/components/svg/visa.vue";

export default {
  name: "rodape",
  components: {
    Instagram,
    MasterCard,
    Facebook,
    PayPal,
    Visa,
  },
};
</script>

<style lang="scss" scoped>
.container {
  justify-content: space-between;
}

svg {
  margin: 0 10px;
}

.footer {
  background: #f9f9f9;
  padding: 40px 10px;
}

.footer p {
  font-size: 1.125em;
  line-height: 1.4em;
  margin: 0 10px;
  flex: 1;
}

.footer-card,
.footer-social {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

@media (max-width: 739px) {
  .footer-img,
  .footer p {
    margin: 10px 0px;
  }

  .footer-row {
    flex-direction: row !important;
  }

  svg {
    width: 30px;
  }
}
</style>
