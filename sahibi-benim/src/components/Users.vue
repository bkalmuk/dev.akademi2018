<template >
  <div>
    <ul class="userList">
      <li :users=users v-for="user in users">
        <p class="card-text">{{user.cityName}}, {{user.education}}, {{user.cityName}}, {{user.job}}, {{user.cityName}}, {{user.martialStatus}}, {{user.age}} </p>
      </li>
    </ul>

    <b-pagination-nav align="center" base-url="#" :number-of-pages="5" v-model="currentPage" />
    <br>
    <div>currentPage: {{currentPage}}</div>

  </div>
</template>

<script>
export default {
  name: 'Users',
   data() {
    return {
      users: [],
      currentPage: 1
    }
  },
  created() {
    this.users = [];
    fetch(`https://devakademi.sahibinden.com/api/users/findAllWithPagination?pageSize=5&currentPage=${this.currentPage}`)
    .then((res) => { return res.json() })
    .then((res) => { this.users = res; })
  }
}
</script>

<style lang="scss">
ul.userList {
  padding-left:0;
  margin:30px;
  border: 1px solid rgb(21, 123, 207);
  li {
    list-style: none;
    border-bottom: 1px solid rgb(21, 123, 207);
    padding-top: 5px;
    padding-bottom: 5px;
  }
}
</style>
