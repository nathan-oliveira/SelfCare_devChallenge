<template>
  <header class="menu" id="header">
    <div class="container">
      <div class="menu-logo">
        <router-link to="/">
          <i class="fas fa-star"></i>
          <p>selfcare</p>
        </router-link>
      </div>
      <nav class="menu-nav">
        <ul>
          <li>
            <router-link to="/">
              <svg
                width="24"
                height="28"
                viewBox="0 0 24 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M10.1023 17.6137C14.577 17.6137 18.2045 13.9862 18.2045 9.51145C18.2045 5.03669 14.577 1.40918 10.1023 1.40918C5.62751 1.40918 2 5.03669 2 9.51145C2 13.9862 5.62751 17.6137 10.1023 17.6137Z"
                  stroke="#5CA720"
                  stroke-width="2.12684"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M23.1365 22.5455L16.0911 15.5"
                  stroke="#5CA720"
                  stroke-width="2.46591"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </router-link>
          </li>
          <li>
            <router-link to="/">
              <svg
                width="24"
                height="28"
                viewBox="0 0 24 23"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M22.6139 25.7784V23.1364C22.6139 21.735 22.0572 20.3909 21.0662 19.4C20.0753 18.409 18.7312 17.8523 17.3298 17.8523H6.76163C5.3602 17.8523 4.01617 18.409 3.02521 19.4C2.03425 20.3909 1.47754 21.735 1.47754 23.1364V25.7784"
                  stroke="#5CA720"
                  stroke-width="2.12684"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M12.0458 12.5682C14.9641 12.5682 17.3299 10.2024 17.3299 7.28409C17.3299 4.36577 14.9641 2 12.0458 2C9.12749 2 6.76172 4.36577 6.76172 7.28409C6.76172 10.2024 9.12749 12.5682 12.0458 12.5682Z"
                  stroke="#5CA720"
                  stroke-width="2.46591"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </router-link>
          </li>
          <li>
            <router-link to="/">
              <svg
                width="24"
                height="28"
                viewBox="0 0 24 19"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M9.64092 22.2894C10.1715 22.2894 10.6017 21.8593 10.6017 21.3287C10.6017 20.7981 10.1715 20.3679 9.64092 20.3679C9.11032 20.3679 8.68018 20.7981 8.68018 21.3287C8.68018 21.8593 9.11032 22.2894 9.64092 22.2894Z"
                  stroke="#5CA720"
                  stroke-width="2.12684"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M20.2093 22.2894C20.7399 22.2894 21.17 21.8593 21.17 21.3287C21.17 20.7981 20.7399 20.3679 20.2093 20.3679C19.6787 20.3679 19.2485 20.7981 19.2485 21.3287C19.2485 21.8593 19.6787 22.2894 20.2093 22.2894Z"
                  stroke="#5CA720"
                  stroke-width="2.46591"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M1.95483 2.11353H5.79781L8.3726 14.9779C8.46046 15.4202 8.70109 15.8175 9.05237 16.1003C9.40366 16.3831 9.84321 16.5333 10.2941 16.5247H19.6325C20.0834 16.5333 20.523 16.3831 20.8742 16.1003C21.2255 15.8175 21.4662 15.4202 21.554 14.9779L23.0912 6.91724H6.75855"
                  stroke="#5CA720"
                  stroke-width="2.46591"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </router-link>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "NavBar",
  props: {
    msg: String,
  },
  mounted() {
    /* eslint-disable func-names */
    const menuHeader = document.getElementById("header");

    window.onscroll = function () {
      const top = window.pageYOffset || document.documentElement.scrollTop;
      if (top > 120) {
        menuHeader.classList.add("fixed");
      } else {
        menuHeader.classList.remove("fixed");
      }
    };
  },
};
</script>

<style scoped lang="scss">
.container {
  align-items: center;
}

.menu {
  background: #ffffff;
  padding: 30px 10px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}

.menu-nav a {
  color: #5ca720;
  font-size: 1.125rem;
}

.menu-logo {
  margin: 0 10px;
}

.menu-logo a {
  font-size: 1.6rem;
  color: #161616;
  font-weight: 700;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  font-family: "Cabin", sans-serif;
}

.menu-logo i {
  font-size: 1.25rem;
  margin-right: 6px;
  margin-top: 4px;
}

.menu-nav {
  flex: 1;
  margin: 0 10px;
  align-self: center;
}

.menu-nav ul {
  float: right;
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

.menu-nav ul li a {
  padding-left: 30px;
}

@media (max-width: 739px) {
  .menu-nav,
  .menu-logo {
    margin: 0 15px;
  }
  .menu-logo a {
    font-size: 1rem;
  }
  .menu-logo i {
    font-size: 0.8rem;
  }
  .container {
    flex-direction: inherit !important;
  }
  svg {
    width: 1rem;
  }
}

@media (max-width: 408px) {
  .menu {
    padding: 20px 20px !important;
  }

  .menu-nav ul li a {
    padding-left: 10px;
  }

  .menu-logo,
  .menu-nav {
    margin: 0 0px;
  }
}

@keyframes animaHeader {
  0% {
    transform: translateY(-100%);
    -webkit-transform: translateY(-100%);
    opacity: 0;
  }

  100% {
    transform: translateY(0%);
    -webkit-transform: translateY(0%);
    opacity: 1;
  }
}

.menu.fixed {
  position: fixed;
  top: 0px;
  width: 100%;
  box-shadow: 0px 0px 5px -1px rgba(0, 0, 0, 0.25);
  animation: animaHeader 0.3s ease-in-out 0.3s backwards;
  -webkit-animation: animaHeader 0.3s ease-in-out 0.3s backwards;
  z-index: 9999;
}
</style>
