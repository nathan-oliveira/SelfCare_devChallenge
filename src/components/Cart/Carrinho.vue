<template>
  <section class="produtos">
    <div class="container">
      <div class="produtos-item" data-anime="left">
        <img src="../../assets/gabrielle-henderson-1DMNn6gBbwQ-unsplash.jpg" />
        <h2>Lorem ipsum dolor sit</h2>
        <h3>R$ <span>50,00</span></h3>
      </div>

      <div class="produtos-item" data-anime="top">
        <img src="../../assets/devin-avery-bMH8ub9z1_U-unsplash.jpg" />
        <h2>Lorem ipsum dolor sit</h2>
        <h3>R$ <span>50,00</span></h3>
      </div>

      <div class="produtos-item" data-anime="right">
        <img src="../../assets/devin-avery-BRVqq2uak4E-unsplash.jpg" />
        <h2>Lorem ipsum dolor sit</h2>
        <h3>R$ <span>50,00</span></h3>
      </div>

      <div class="produtos-item" data-anime="top">
        <img src="../../assets/nery-montenegro-SmEty_TVr80-unsplash.jpg" />
        <h2>Lorem ipsum dolor sit</h2>
        <h3>R$ <span>50,00</span></h3>
      </div>

      <div class="produtos-item" data-anime="left">
        <img src="../../assets/olena-sergienko-GOVTETevRm8-unsplash.jpg" />
        <h2>Lorem ipsum dolor sit</h2>
        <h3>R$ <span>50,00</span></h3>
      </div>

      <div class="produtos-item" data-anime="top">
        <img src="../../assets/pharma-hemp-complex-tAzdKblAinw-unsplash.jpg" />
        <h2>Lorem ipsum dolor sit</h2>
        <h3>R$ <span>50,00</span></h3>
      </div>

      <div class="produtos-item" data-anime="right">
        <img src="../../assets/phaedra-botanicals-uFAHrKYkTVI-unsplash.jpg" />
        <h2>Lorem ipsum dolor sit</h2>
        <h3>R$ <span>50,00</span></h3>
      </div>

      <div class="produtos-item" data-anime="top">
        <img src="../../assets/pharma-hemp-complex-yVAXSK6zFIM-unsplash.jpg" />
        <h2>Lorem ipsum dolor sit</h2>
        <h3>R$ <span>50,00</span></h3>
      </div>

      <div class="produtos-item" data-anime="right">
        <img src="../../assets/chandra-oh-y5hRv6UNKMg-unsplash.jpg" />
        <h2>Lorem ipsum dolor sit</h2>
        <h3>R$ <span>50,00</span></h3>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Carrinho",
  mounted() {
    /* eslint-disable prefer-arrow-callback, no-console, func-names, no-use-before-define, comma-dangle */
    const target = document.querySelectorAll("[data-anime]");
    function animeScroll() {
      const windowTop = window.pageYOffset + window.innerHeight * 0.75;
      target.forEach(function (element) {
        if (windowTop > element.offsetTop) {
          element.classList.add("animate");
        } else {
          element.classList.remove("animate");
        }
      });
    }
    animeScroll();
    if (target.length) {
      window.addEventListener("scroll", function () {
        animeScroll();
      });
    }
  },
};
</script>

<style lang="scss" scoped>
[data-anime] {
  opacity: 0;
  transition: 0.3s;
}

[data-anime="left"] {
  transform: translate3d(-50px, 0, 0);
}

[data-anime="right"] {
  transform: translate3d(0, -50px, 0);
}

[data-anime="top"] {
  transform: translate3d(50px, 0, 0);
}

[data-anime].animate {
  opacity: 1;
  transform: translate3d(0px, 0px, 0px);
}

.container {
  justify-content: space-between;
  flex-wrap: wrap;
}

.produtos {
  margin: 0 10px;
}

.produtos-item {
  flex: 1 1 25%;
  margin: 10px;
  max-width: 403px;
  max-height: 403px;
}

.produtos-item:nth-of-type(3n + 2) {
  text-align: center;
}
.produtos-item:nth-of-type(3n + 2) h2,
.produtos-item:nth-of-type(3n + 2) h3 {
  text-align: start;
  margin-left: 50px;
}

.produtos-item:nth-of-type(3n + 3) {
  text-align: end;
}

.produtos-item:nth-of-type(3n + 3) h2,
.produtos-item:nth-of-type(3n + 3) h3 {
  text-align: initial;
  margin-left: 100px;
}

.produtos-item img {
  background: no-repeat center;
  background-size: cover;
  width: 100%;
  max-width: 303px;
  height: 303px;
  border-radius: 3%;
  margin-top: 45px;
  margin-bottom: 9px;
}

.produtos-item h2,
.produtos-item h3 {
  font-size: 1.2rem;
  color: #161616;
  font-weight: 400;
  margin-top: 5px;
  font-family: "Lato", sans-serif;
}

.produtos-item h3 span {
  font-size: 1.2rem;
  color: #5ca720;
}

.produtos-item h3 {
  font-size: 1rem;
}

@media (max-width: 1111px) {
  .produtos-item h2,
  .produtos-item h3 {
    font-size: 1rem;
  }

  .produtos-item:nth-of-type(3n + 2) h2,
  .produtos-item:nth-of-type(3n + 2) h3 {
    text-align: initial;
    margin-left: 0px !important;
  }
  .produtos-item:nth-of-type(3n + 3) h2,
  .produtos-item:nth-of-type(3n + 3) h3 {
    text-align: initial;
    margin-left: 0px !important;
  }
}

@media (max-width: 739px) {
  .produtos-item {
    flex: 1 1 30%;
    max-width: 40%;
  }
  .container {
    flex-direction: inherit;
  }
  .produtos-item h2 {
    font-size: 0.8rem;
  }
  .produtos-item:nth-of-type(3n + 2) {
    text-align: center;
    // margin-left: 0px !important;
  }

  .produtos-item:nth-of-type(3n + 3) {
    text-align: initial;
  }

  .produtos-item img {
    height: 170px;
  }
}

@media (max-width: 409px) {
  .produtos {
    margin: 0 20px;
  }
  .produtos-item {
    margin: 6px;
  }

  .produtos-item img {
    height: 140px;
    margin-top: 20px;
  }

  .produtos-item h2,
  .produtos-item h3 {
    font-size: 0.74rem;
  }
}

@media (max-width: 331px) {
  .produtos-item h2,
  .produtos-item h3 {
    font-size: 0.6rem;
  }
}
</style>
