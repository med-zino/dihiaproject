<template>
  <nav class="navbar">
    <div></div>
    <h2 class="logo">{{ logoText }}</h2><span class="logo">@Dihia_moussi</span>
    <ul class="nav-menu">
      <li v-for="item in navItems" :key="item.name" class="nav-item">
        <a :href="item.href">{{ item.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Nav-bar',
  data() {
    return {
      logoText: 'DM',
      navItems: [
        { name: 'Home', href: '/' },
        { name: 'Trophy', href: '/trophy' },
        { name: 'Accounts', href: '/accounts' }
      ]
    }
  }
}
</script>

<style scoped>
.navbar {
  display: flex;
  align-items: center;
  padding: 10px 76px 10px 74px;
  color: #333;
  

}
span {
    color: rgb(244, 52, 84);
}
.logo {
  font-family: 'Dancing Script', cursive;
  margin-right: auto;
}

.nav-menu {
  list-style: none;
  display: flex;
}

.nav-item {
  margin-left: 60px;
}

.nav-item a {
    color: #333;
  text-decoration: none;
}



.nav-item a:hover {
  text-decoration: underline;
  color: red;
}
</style>
