<template>
  <div>
    <b-navbar  type="dark" variant="primary" toggleable>
      <b-navbar-toggle target="nav_dropdown_collapse"></b-navbar-toggle>
      <b-collapse is-nav id="nav_dropdown_collapse">
        <b-navbar-nav>
          <b-nav-item href="#" class="nav">Kullanıcılar</b-nav-item>
          <b-nav-item href="#">Kategoriler</b-nav-item>
          <b-nav-item href="#">Yaş aralığı</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'Navnav'
}
</script>

<style lang="scss">

</style>
