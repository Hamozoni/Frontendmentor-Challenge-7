<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/logo.svg" alt="" class="logo" />
      </div>
      <div @click="toggle" class="burger">
        <span></span>
        <span></span>
        <span></span>
      </div>
      <transition name="menu-fade">
        <div class="menu" v-bind:class="showMenu && 'Show-menu'">
          <ul>
            <li><a href="#">Features</a></li>
            <li><a href="#">Pricing</a></li>
            <li><a href="#">Resources</a></li>
          </ul>
          <div class="loging">
            <button id="login">Login</button>
            <button id="signUp">Sign Up</button>
          </div>
        </div>
      </transition>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComp",
  data() {
    return {
      showMenu: false,
    };
  },
  methods: {
    toggle() {
      this.showMenu = !this.showMenu;
    },
  },
};
</script>

<style>
header .container {
  position: relative;
  padding: 40px 15px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 60px;
}
.container .menu .loging #signUp {
  margin-top: 10px;
  background-color: var(--cyan);
  color: #fff;
}
@media (max-width: 767px) {
  .burger {
    cursor: pointer;
  }
  .burger span {
    display: block;
    background: var(--gray);
    height: 4px;
    width: 25px;
    margin-bottom: 4px;
  }
  header .container .menu {
    display: none;
    position: absolute;
    background-color: var(--dark-violet);
    width: 98%;
    top: 100px;
    padding: 30px;
    border-radius: 10px;
    text-align: center;
    z-index: 999;
  }
  header .container .menu.Show-menu {
    display: block;
  }
  header .container .menu ul li {
    padding: 10px;
  }
  .menu-fade-enter-from {
    opacity: 0;
    transform: translateY(-100%);
  }
  .menu-fade-enter-to {
    opacity: 1;
    transform: translateY(0);
  }
  .menu-fade-enter-active {
    transition: all 2s ease;
  }
  header .container .menu ul li a {
    color: var(--weight);
  }
  header .container .menu ul li a:hover {
    color: var(--gray);
  }
  .container .menu .loging {
    margin-top: 30px;
    padding-top: 30px;
    border-top: 1px solid hsl(0deg 0% 37%);
  }
  .container .menu .loging button {
    display: block;
    text-align: center;
    width: 100%;
    padding: 10px 20px;
    color: var(--grayish-violet);
    background-color: transparent;
    border-radius: 20px;
    font-weight: 700;
  }
  .container .menu .loging button:hover {
    background-color: var(--cyan);
    color: #fff;
  }
}
@media (min-width: 768px) {
  header .container .menu {
    flex: 1;
    display: flex;
    justify-content: space-between;
  }
  header .container .menu ul {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    gap: 30px;
    flex: 1;
  }
  header .container .menu ul li a {
    color: var(--grayish-violet);
  }
  header .container .menu ul li a:hover {
    color: var(--very-dark-violet);
  }
  .container .menu .loging button {
    padding: 10px 20px;
    color: var(--grayish-violet);
    background-color: transparent;
    border-radius: 20px;
  }
}
</style>
