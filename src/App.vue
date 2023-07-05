<template>
  <div id="app">
    <header>
      <nav>
        <ul>
          <li :class="{ active: $route.path === '/' }"><router-link to="/">Weather</router-link></li>
          <li :class="{ active: $route.path === '/location' }"><router-link to="/location">Location</router-link></li>
          <li :class="{ active: $route.path === '/stopwatch' }"><router-link to="/stopwatch">Stopwatch</router-link></li>
          <li :class="{ active: $route.path === '/tictactoe' }"><router-link to="/tictactoe">Tic Tac Toe</router-link></li>
          <li :class="{ active: $route.path === '/photo' }"><router-link to="/photo">Photo</router-link></li>
        </ul>
      </nav>
    </header>
    <router-view></router-view>
  </div>
</template>

<style>
#app {
  text-align: center;
}

header {
  background: blue;
  padding: 20px;
}
body{
  background-color: #068FFF;
}
nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

nav li {
  display: inline-block;
  margin-right: 10px;
}

nav a {
  color: #fff;
  text-decoration: none;
  padding: 5px 10px;
}

nav a:hover {
  text-decoration: underline;
}

/* Tambahkan gaya untuk navigasi aktif */
nav li.active {
  background-color: #000000;
}
</style>
