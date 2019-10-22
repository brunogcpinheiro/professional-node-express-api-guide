<template>
  <aside id="sidebar">
    <h3>Steps</h3>

    <ol>
      <li v-for="item in menu" :key="item.title">
        <p>
          <nuxt-link :to="item.route" exact>
            <a>{{ item.title }}</a>
          </nuxt-link>
        </p>
      </li>
    </ol>
  </aside>
</template>

<script>
export default {
  name: "Sidebar",
  data() {
    return {
      menu: [
        {
          route: '/',
          title: 'Home'
        },
        {
          route: '/getting-started',
          title: 'Getting Started'
        },
      ],
      isActive: false
    };
  }
}
</script>

<style scoped>
#sidebar {
  min-height: calc(100vh - 70px);
  height: 100%;
  background: #ebebeb;
  border-right: 3px solid #bcf5c6;
  padding: 20px;
}

h4 {
  text-decoration: underline;
}

ol {
  padding: 10px;
  font-weight: bold;
  font-size: 0.9rem;
}

li {
  margin-top: 10px;
}

a {
  cursor: pointer;
  font-weight: bold;
  font-size: 0.9rem;
}

a:link, a:visited {
  text-decoration: none;
  color: #181818;
}

a:hover {
  border-bottom: 3px solid #2acf2a;
}

</style>