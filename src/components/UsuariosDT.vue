<template>
  <div>
    <h1>Usuarios</h1>
    <v-data-table
      :loading="cargando"
      loading-text="Loading... Please wait"
      :headers="headers"
      :items="usuarios"
      sort-by="rol"
      class="elevation-1"
      >-
      <template v-slot:top>
        <v-toolbar flat>
          <v-toolbar-title>Listado Usuarios</v-toolbar-title>
          <v-divider class="mx-4" inset vertical></v-divider>
          <v-spacer></v-spacer>
          <v-dialog v-model="dialog" max-width="500px">
            <template v-slot:activator="{ on, attrs }">
              <v-btn color="primary" dark class="mb-2" v-bind="attrs" v-on="on">
                Crear Usuario
              </v-btn>
            </template>
            <v-card>
              <v-card-title>
                <span class="text-h5">{{ formTitle }}</span>
              </v-card-title>

              <v-card-text>
                <v-container>
                  <v-row>
                    <v-col cols="12" sm="6" md="4">
                      <v-text-field
                        v-model="editedItem.nombre"
                        label="Nombre"
                      ></v-text-field>
                    </v-col>

                    <v-col 
                    v-if="editedIndex === -1"
                    cols="12" sm="6" md="4">
                      <v-text-field
                        v-model="editedItem.correo"
                        label="Correo"
                      ></v-text-field>
                    </v-col>

                    <v-col cols="12" sm="6" md="4">
                      <v-select
                        v-model="editedItem.rol"
                        label="Rol"
                        :items="roles"
                      ></v-select>
                    </v-col>

                    <v-col cols="12" sm="6" md="4">
                      <v-text-field
                        v-model="editedItem.password"
                        label="Contraseña"
                      ></v-text-field>
                    </v-col>

                    <!-- <v-col cols="12" sm="6" md="4">
                      <v-text-field
                        v-model="editedItem._id"
                        label="Identificador"
                      ></v-text-field>
                    </v-col> -->

                  </v-row>
                </v-container>
              </v-card-text>

              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="blue darken-1" text @click="close">
                  Cancelar
                </v-btn>
                <v-btn color="blue darken-1" text @click="save">
                  Guardar
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-dialog>
          <v-dialog v-model="dialogDelete" max-width="500px">
            <v-card>
              <v-card-title class="text-h5"
                >Are you sure you want to delete this item?</v-card-title
              >
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="blue darken-1" text @click="closeDelete"
                  >Cancel</v-btn
                >
                <v-btn color="blue darken-1" text @click="deleteItemConfirm"
                  >OK</v-btn
                >
                <v-spacer></v-spacer>
              </v-card-actions>
            </v-card>
          </v-dialog>
        </v-toolbar>
      </template>

      <template v-slot:[`item.actions`]="{ item }">
        <v-icon small class="mr-2" @click="editItem(item)">
          mdi-pencil
        </v-icon>
        <v-icon small @click="deleteItem(item)">
          mdi-delete
        </v-icon>
      </template>
      
      <template v-slot:no-data>
        <v-btn color="primary" @click="initialize">
          Reset
        </v-btn>
      </template>
    </v-data-table>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data: () => ({
    dialog: false,
    cargando: true,
    dialogDelete: false,
    headers: [
      { text: "ID", value: "_id", sortable: false },
      {
        text: "Nombre",
        align: "start",
        sortable: false,
        value: "nombre",
      },
      { text: "Correo", value: "correo" },
      { text: "Rol", value: "rol" },
      { text: "Estado", value: "Estado" },
      { text: "Actions", value: "actions", sortable: false },
    ],
    desserts: [],
    usuarios: [],
    roles: ['Administrador', 'Terapeuta'],
    editedIndex: -1,
    editedItem: {
      _id: "",
      nombre: "",
      correo: "",
      rol: "Terapeuta",
      password: "",
    },
    defaultItem: {
      _id: "",
      nombre: "",
      correo: "",
      rol: "Terapeuta",
      password: "",
    },
  }),

  computed: {
    formTitle() {
      return this.editedIndex === -1 ? "Nuevo Usuario" : "Editando Usuario";
    },
  },

  watch: {
    dialog(val) {
      val || this.close();
    },
    dialogDelete(val) {
      val || this.closeDelete();
    },
  },

  created() {
    // this.initialize();
    this.list();
  },

  methods: {
    // initialize() {
    //   this.usuarios = [
    //     {
    //       _id: "Frozen Yogurt",
    //       nombre: 159,
    //       correo: 6.0,
    //       rol: 24,
    //       Estado: 1,
    //       password: "djfkdfijioejf"
    //     }
    //   ];
    // },

    list() {
      axios.get('http://localhost:3000/api/usuario/list')
        .then((response) => {
          // handle success
          this.usuarios = response.data;
          this.cargando = false;
          // console.log(response);
        })
        .catch(error => {
          // handle error
          console.log(error);
        })
    },

    editItem(item) {
      this.editedIndex = this.usuarios.indexOf(item);
      this.editedItem = Object.assign({}, item);
      this.dialog = true;
    },

    deleteItem(item) {
      this.editedIndex = this.usuarios.indexOf(item);
      this.editedItem = Object.assign({}, item);
      this.dialogDelete = true;
    },

    deleteItemConfirm() {

      if(this.editedItem.estado === 1){
        axios.put('http://localhost:3000/api/usuario/disabled', {
          estado: 0,
          _id: this.editedItem._id,
        })
        .then(response => {
          this.list();
        })
        .catch(error => {
          console.log(error);
        })
      }else{
        axios.put('http://localhost:3000/api/usuario/enabled', {
          estado: 1,
          _id: this.editedItem._id,
        })
        .then(response => {
          this.list();
        })
        .catch(error => {
          console.log(error);
        })
      }
      this.closeDelete();
    },

    close() {
      this.dialog = false;
      this.$nextTick(() => {
        this.editedItem = Object.assign({}, this.defaultItem);
        this.editedIndex = -1;
      });
    },

    closeDelete() {
      this.dialogDelete = false;
      this.$nextTick(() => {
        this.editedItem = Object.assign({}, this.defaultItem);
        this.editedIndex = -1;
      });
    },

    save() {
      if (this.editedIndex > -1) {
        Object.assign(this.usuarios[this.editedIndex], this.editedItem);

        axios.put('http://localhost:3000/api/usuario/update', {
          nombre: this.editedItem.nombre,
          correo: this.editedItem.correo,
          rol : this.editedItem.rol,
          password : this.editedItem.password,
        })
        .then(response => {
          this.list();
        })
        .catch(error => {
          console.log(error);
        })

      } else {
        // this.usuarios.push(this.editedItem);
        axios.post('http://localhost:3000/api/usuario/add', {
          nombre: this.editedItem.nombre,
          correo: this.editedItem.correo,
          rol : this.editedItem.rol,
          password : this.editedItem.password,
        })
        .then(response => {
          this.list();
        })
        .catch(error => {
          console.log(error);
        })
      }
      this.close();
    },
  },
};
</script>
