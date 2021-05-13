<template>
  <div id="app">
    <b-table striped hover :items="items" :fields="fields"></b-table>
  </div>
</template>
<script>
export default {
  data() {
    return {
      fields: [
        {
          key: "lastName",
          sortable: true,
          label: "Last"
        },
        {
          key: "firstName",
          sortable: false,
          label: "First"
        }
      ],
      items: [
        { firstName: "alex", lastName: "green" },
        {
          firstName: "may",
          lastName: "smith"
        },
        { firstName: "james", lastName: "jones" }
      ]
    };
  }
};
</script>


addRow() {
    this.rows.push({
      row: []
    });
  },
  removeRow: function(index) {
    console.log("Removing", index);
    this.rows.splice(index, 1);
  }
  
  
  <template>
  <b-container class="mt-4">
    <b-table :items="items" :current-page="currentPage" :per-page="perPage" striped></b-table>

    <b-pagination v-model="currentPage" :total-rows="items.length" :per-page="perPage"></b-pagination>
  </b-container>
</template>

<script>
const itemCount = 15000;
const items = Array.from({ length: itemCount }, (v, i) => ({
  isActive: i % 2 === 0,
  age: i,
  first_name: `Dickerson ${i}`,
  last_name: `Macdonald ${i}`
}));

export default {
  data() {
    return {
      items,
      currentPage: 0,
      perPage: 10
    };
  }
};
</script>
