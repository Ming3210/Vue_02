<template>
  <div class="app-container">
    <h1 class="side">B9</h1>
    <h1>User Management</h1>
    <table>
      <thead>
        <tr>
          <th>STT</th>
          <th>Họ và tên</th>
          <th>Ngày sinh</th>
          <th>Giới tính</th>
          <th>Địa chỉ</th>
          <th>Hành động</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(user, index) in users" :key="user.id">
          <td data-label="STT">{{ index + 1 }}</td>
          <td data-label="Họ và tên">{{ user.name }}</td>
          <td data-label="Ngày sinh">{{ user.dob }}</td>
          <td data-label="Giới tính">{{ user.gender }}</td>
          <td data-label="Địa chỉ">{{ user.address }}</td>
          <td data-label="Hành động">
            <button class="action-btn edit-btn" @click="editUser(user.id)">Sửa</button>
            <button class="action-btn delete-btn" @click="deleteUser(user.id)">Xóa</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'App',
  setup() {
    const users = ref([
      { id: 1, name: 'Malcolm Lockyer', dob: '21/03/1961', gender: 'Nam', address: 'New York' },
      { id: 2, name: 'Maria', dob: '11/02/1990', gender: 'Nữ', address: 'London' },
    ])

    const editUser = (id) => {
      console.log('Edit user with id:', id)
      // Implement edit logic here
    }

    const deleteUser = (id) => {
      console.log('Delete user with id:', id)
      // Implement delete logic here
    }

    return {
      users,
      editUser,
      deleteUser
    }
  }
}
</script>

<style scoped>
.app-container {
  font-family: Arial, sans-serif;
  max-width: 100%;
  margin: 0 auto;
  padding: 20px;
}

h1 {
  color: #333;
  text-align: center;
}

.side{
    display: flex;
    justify-content: start;
}

table {
  width: 100%;
  border-collapse: collapse;
  color: #333;
}

thead {
  background-color: #f8f9fa;
}

th {
  padding: 12px;
  text-align: left;
  border-bottom: 2px solid #dee2e6;
  font-weight: bold;
  color: #495057;
}

td {
  padding: 12px;
  border-bottom: 1px solid #dee2e6;
}

tr:nth-child(even) {
  background-color: #f8f9fa;
}

.action-btn {
  padding: 6px 12px;
  margin: 0 4px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 14px;
}

.edit-btn {
  background-color: #ffc107;
  color: #212529;
}

.delete-btn {
  background-color: #dc3545;
  color: #fff;
}

@media (max-width: 768px) {
  table, thead, tbody, th, td, tr {
    display: block;
  }
  
  thead tr {
    position: absolute;
    top: -9999px;
    left: -9999px;
  }
  
  tr {
    margin-bottom: 15px;
  }
  
  td {
    border: none;
    position: relative;
    padding-left: 50%;
  }
  
  td:before {
    position: absolute;
    top: 6px;
    left: 6px;
    width: 45%;
    padding-right: 10px;
    white-space: nowrap;
    content: attr(data-label);
    font-weight: bold;
  }
}
</style>