<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/test1">About</router-link>
  </nav>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
.container {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  height: 100vh;
}

#startButton {
  padding: 10px 20px;
}

#popupWrapper {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  align-items: center;
  justify-content: center;
  display: flex;
}

#popup {
  background-color: #fff;
  padding: 20px;
}

.input-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.input-container input {
  width: calc(50% - 5px);
}
input {
  margin-bottom: 10px;
}
@media (max-width: 500px) {
  .input-container {
    flex-direction: column;
  }

  .input-container input {
    width: 100%;
  }
}
</style>
