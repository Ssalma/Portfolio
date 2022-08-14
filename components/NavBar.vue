<template>
  <nav>
    <div class="logo">
      <NuxtLink to="/">
        <img src="@/assets/Logo.svg" alt="" class="logo-img" />
      </NuxtLink>
    </div>
    <div class="nav__menu">
      <label for="menu" class="label">Menu</label>
      <input id="menu" type="checkbox" />
      <ul class="nav-items">
        <li><NuxtLink class="link" to="/Project">My Projects</NuxtLink></li>
        <li>
          <a
            href="https://docs.google.com/document/d/1ifCkqXpfaGeRbx8Xt0gIH70hYKUkol61wOkv--CcyNE/edit?usp=sharing"
            target="_blank"
            class="link"
            >My Resume</a
          >
        </li>
        <li><NuxtLink to="/contactMe" class="link">Contact me</NuxtLink></li>
      </ul>
    </div>
  </nav>
</template>
<style scoped>
::root {
  --primary: #161b22;
  --secondary: #4284ff;
}
.link.nuxt-link-exact-active {
  background: #4284ff;
  padding: 10px 12px;
  border-radius: 30px;
}
nav {
  width: 100%;
  height: 100px;
  padding: 0 10px;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: #161b22;
  position: sticky;
  top: 0;
  z-index: 100;
  -webkit-box-shadow: 4px 8px 19px -3px rgba(0, 0, 0, 0.27);
  box-shadow: 4px 8px 19px -3px rgba(0, 0, 0, 0.27);
}

.logo-text {
  font-weight: 500;
  font-size: 24px;
}
.link {
  border: 1px solid white;
  padding: 10px 12px;
  border: unset;
  border-radius: 30px;
  z-index: 1;
  background: transparent;
  position: relative;
  font-weight: 1000;
  font-size: 17px;
  transition: all 250ms;
  overflow: hidden;
}
.link::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 0;
  border-radius: 30px;
  background-color: #4284ff;
  z-index: -1;
  transition: all 250ms;
}
.link:hover {
  background: #4284ff;
}

.link:hover::before {
  width: 100%;
}
li a {
  text-decoration: none;
  font-weight: 300;
  color: #ffffff;
  font-style: normal;
  font-size: 16px;
  line-height: 36px;
}
ul {
  display: none;
}
ul,
li {
  list-style-type: none;
  text-decoration: none;
}
#menu:checked ~ .nav-items {
  display: grid;
  place-content: center;
  grid-gap: 50px;
  position: absolute;
  top: 80px;
  right: 0;
  width: 100%;
  height: calc(100vh - 80px);
  background: rgba(196, 216, 254, 1);
}
.label {
  display: block;
  color: #c4d8fe;
  font-size: 18px;
}
#menu {
  display: none;
}
@media screen and (min-width: 768px) {
  #menu:checked ~ .nav-items {
    display: none;
  }
  nav {
    padding: 0 30px;
  }
  li a {
    color: #ffffff;
    text-decoration: none;
    font-weight: 300;
    margin-left: 30px;
    font-style: normal;
    font-size: 16px;
    line-height: 26px;
  }
  #menu {
    display: none;
  }
  .label {
    display: none;
  }
  ul {
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
</style>