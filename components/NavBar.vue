<template>
  <nav>
    <div class="logo">
      <img src="@/assets/Logo.svg" alt="" />
    </div>
    <div class="nav__menu">
      <label for="menu" class="label">Menu</label>
      <input id="menu" type="checkbox" />
      <ul class="nav-items">
        <li><NuxtLink to="/Project">My Projects</NuxtLink></li>
        <li>
          <a
            href="https://docs.google.com/document/d/1ifCkqXpfaGeRbx8Xt0gIH70hYKUkol61wOkv--CcyNE/edit?usp=sharing"
            target="_blank"
            >My Resume</a
          >
        </li>
        <li><NuxtLink to="/">Contact me</NuxtLink></li>
      </ul>
    </div>
  </nav>
</template>
<style scoped>
::root {
  --primary: #161b22;
}
nav {
  width: 100%;
  height: 80px;
  padding: 0 10px;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: #161b22;
  position: sticky;
  top: 0;
}
.logo-text {
  font-weight: 500;
  font-size: 24px;
}
li a {
  text-decoration: none;
  font-weight: 500;
  color: #4284ff;
  font-style: normal;
  font-size: 26px;
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
    color: white;
    text-decoration: none;
    font-weight: 400;
    margin-left: 30px;
    font-style: normal;
    font-size: 16px;
    line-height: 22px;
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
  }
}
</style>