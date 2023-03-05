<template>
  <nav class="nav">
    <div class="container">
      <div class="nav-list">
        <router-link class="nav-item" exact-active-class="active" to="/"
          >Бренд</router-link
        >
        <router-link class="nav-item" exact-active-class="active" to="/content"
          >Контент</router-link
        >
        <router-link class="nav-item" exact-active-class="active" to="/design"
          >Дизайн</router-link
        >
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  name: "navBar",
};
</script>
