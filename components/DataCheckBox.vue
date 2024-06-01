<template>
    <v-data-table :headers="headers" :items="arrData">
      <template #item.indx="{ index }">
        {{ index + 1 }}
      </template>
      <template #item.amount="{ item }">
        <v-text-field
          v-model="item.amount"
          type="number"
          hide-details="auto"
          dense
          style="width: 50px"
        ></v-text-field>
      </template>
    </v-data-table>
  </template>
  
  <script>
  export default {
    data() {
      return {
        headers: [
          { text: 'Index', value: 'indx' },
          { text: 'Amount', value: 'amount' }
        ],
        arrData: [
          { indx: 1, amount: 10 },
          { indx: 2, amount: 20 },
          { indx: 3, amount: 30 }
        ]
      };
    }
  };
  </script>
  
<!-- <template>
    <div>
      <v-data-table
        :headers="headers"
        :items="items"
        :rows-per-page-items="[10, 25, 50, 100]"
        show-select
        item-key="id"
        v-model="selectedItems"
      >
        <template v-slot:top>
          <v-toolbar flat>
            <v-toolbar-title>Select Items</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn @click="getSelectedItems">Get Selected Items</v-btn>
          </v-toolbar>
        </template>
      </v-data-table>
    </div>
  </template>
  
  <script>
  export default {
    name:'DataCheckbox',
    data() {
      return {
        headers: [
          { text: 'ID', value: 'id' },
          { text: 'Name', value: 'name' },
          { text: 'Email', value: 'email' }
        ],
        items: [
          { id: 1, name: 'John Doe', email: 'john@example.com' },
          { id: 2, name: 'Jane Smith', email: 'jane@example.com' },
          { id: 3, name: 'Bob Johnson', email: 'bob@example.com' }
        ],
        selectedItems: []
      };
    },
    methods: {
      getSelectedItems() {
        console.log(this.selectedItems);
      }
    }
  };
  </script> -->