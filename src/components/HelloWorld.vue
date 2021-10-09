<template>
  <div class="users-table table-wrapper">
    <table class="posts-table table">
      <thead>
        <tr class="users-table-info">
          <th>ID</th>
          <th>NAME</th>
          <th>USER NAME</th>
          <th>EMAIL</th>
          <th>PHONE</th>
          <th>STATUS</th>
          <th>WEB</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in info" :key="item">
          <td>{{ item.id }}</td>
          <td>{{ item.name }}</td>
          <td>{{ item.username }}</td>
          <td>{{item.email}}</td>
          <td>{{item.phone}}</td>
          <td><span class="badge-pending">Pending</span></td>
          <td>{{item.website}}</td>
          
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import Loading from "vue-loading-overlay";
import "vue-loading-overlay/dist/vue-loading.css";
import axios from "axios";
export default {
  name: "HelloWorld",
  components: {
    Loading,
  },
  data() {
    return {
      info: null
    };
  },
  mounted() {
    axios
      .get("https://jsonplaceholder.typicode.com/users")
      .then((response) => (this.info = response.data));
      if (this.info==null) {
        
      } else {
        
      }
  },
};
</script>
