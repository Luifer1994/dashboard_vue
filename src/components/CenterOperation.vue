<template>
  <div class="users-table table-wrapper">
    <table class="posts-table table">
      <thead>
        <tr class="users-table-info">
          <th>ID</th>
          <th>NAME</th>
          <th>STATUS</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in info" :key="item">
          <td>{{ item.cod_erp }}</td>
          <td>{{ item.descripcion }}</td>
          <td v-if="item.ind_estado == 'HABILITADO'"><span class="badge-active">{{ item.ind_estado }}</span></td>
          <td v-else><span class="badge-trashed">{{ item.ind_estado }}</span></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "CenterOperation",
  data() {
    return {
      info: []
    };
  },
  mounted() {
    axios
      .post("https://api-wsdl.acercate.com.co/centrosOpByCompany")
      .then((response) => (this.info = response.data.data));
  },
};
</script>
