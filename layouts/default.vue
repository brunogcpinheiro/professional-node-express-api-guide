<template>
  <div id="layout">
    <Header/>
    <Sidebar/>
    <main class="main">
      <Nuxt/>
    </main>
  </div>
</template>

<script>
import Header from "@/components/Header";
import Sidebar from "@/components/Sidebar";

export default {
  components: {
    Header,
    Sidebar
  }
};
</script>


<style>
@import url("https://fonts.googleapis.com/css?family=Lexend+Deca|Quicksand:200,400,700&display=swap");

html {
  font-family: "Quicksand", Arial, sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Lexend Deca", "Quicksand", Arial, sans-serif;
  color: #31b351;
}

p {
  font-family: "Quicksand", "Lexend Deca", Arial, sans-serif;
  font-size: 16px;
  line-height: 2;
}

ul {
  list-style: none;
}

a,
button {
  cursor: pointer;
}

.word {
  padding: 7px;
  background: #dddddd;
  color: #31b351;
  font-weight: bold;
  border-radius: 7px;
}

#layout {
  display: grid;
  grid-template-columns: 1fr 4fr;
  grid-template-rows: 1fr;
  grid-template-areas:
    "header header"
    "aside main";
}

header {
  grid-area: header;
}
aside {
  grid-area: aside;
}
main {
  grid-area: main;
  width: 100%;
}

::-webkit-scrollbar-thumb {
  background: #5eb362;
  width: 5;
  border-radius: 20px;
}
::-webkit-scrollbar {
  width: 7px;
  height: 8px;
  background-color: #abdbaf; /* or add it to the track */
}

.container {
  min-height: calc(100vh - 70px);
  height: 100%;
  background: #fff;
  padding: 20px;
}

.active-link {
  border-bottom: 3px solid #2acf2a;
}

pre.language-javascript {
  margin: 20px 0;
  padding: 10px;
  display: flex;
  width: 70%;
  border-radius: 7px;
  border: 1px dashed #50da50;
  background: #d1e9d0;
}

code.language-javascript {
  background: transparent;
  font-family: "Quicksand", sans-serif;
  font-weight: bold;
  font-size: 0.875rem;
}
</style>
