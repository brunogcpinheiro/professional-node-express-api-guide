<template>
  <div id="layout">
    <Header />
    <div class="content">
      <Sidebar />
      <main>
        <Nuxt/>
      </main>
    </div>
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
@import url("https://fonts.googleapis.com/css?family=Lexend+Deca|Montserrat:200,400,700&display=swap");

html {
  font-family: "Montserrat", Arial, sans-serif;
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
  font-family: "Lexend Deca", "Montserrat", Arial, sans-serif;
}

p {
  font-family: "Montserrat", "Lexend Deca", Arial, sans-serif;
  font-size: 12px;
}

#layout {
  display: flex;
  flex-direction: column;
}

.content {
  display: flex;
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
</style>
