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