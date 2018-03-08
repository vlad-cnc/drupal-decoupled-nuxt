<template>
  <header>
    <nav>
      <ul>
        <li><nuxt-link to="/" >Starting Page</nuxt-link></li>
        <li><nuxt-link to="/recipes" >Recipes</nuxt-link></li>
        <li><nuxt-link to="/about" >About</nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>
<style>
  header {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 30px;
  }
  ul {
    padding:0;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  li {
    margin: 0 10px;
    background: cornflowerblue;
    color: white;
    border-radius: 5px;
  }
  a {
    text-decoration: none;
    color: white;
    padding: 10px;
  }
</style>