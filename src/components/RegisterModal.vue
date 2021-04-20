<template>
  <q-dialog :value="true">
    <q-card class="card text-white">
      <q-card-section>
        <div class="text-h6">Register</div>
      </q-card-section>

      <q-card-section class="card-section">
        <q-input
          class="q-mb-md"
          color="orange-4"
          standout
          v-model="email"
          label="E-mail"
          clearable
        >
          <template v-slot:prepend>
            <i class="fas fa-envelope"></i>
          </template>
        </q-input>
        <q-input
          class="q-mb-md"
          color="orange-4"
          standout
          v-model="fullname"
          label="Name"
          clearable
        >
          <template v-slot:prepend>
            <i class="fas fa-user-edit"></i>
          </template>
        </q-input>
        <q-input
          class="q-mb-md"
          color="orange-4"
          standout
          v-model="password"
          label="Password"
          clearable
        >
          <template v-slot:prepend>
            <i class="fas fa-key"></i>
          </template>
        </q-input>
      </q-card-section>

      <q-card-actions class="card-section" align="right">
        <q-btn class="button" flat label="Register" v-close-popup />
        <q-btn class="button" flat label="Cancel" v-close-popup />
      </q-card-actions>
    </q-card>
  </q-dialog>
</template>

<script>
export default {
  name: "RegisterModal",
  data() {
    return {
      email: "",
      fullname: "",
      password: ""
    };
  }
};
</script>

<style scoped>
.card {
  background-color: #f7971e;
  width: 30vw;
}

.card-section {
  background-color: white;
}
.button {
  background-color: white;
  color: #f7971e;
}
</style>
