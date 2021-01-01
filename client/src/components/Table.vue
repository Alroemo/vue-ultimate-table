<template>
  <div>
    <b-card title="Table Name" class='tableCard' tag="article">
      <b-card-text>
        Some quick example text to build on the card title and make up the bulk of the card's content.
      </b-card-text>

      <div class="toolbar text-right">
        
        <b-button v-b-tooltip.hover title="Tooltip directive content">
          Hover Me
        </b-button>

        <b-button id="tooltip-target-1">
          Hover Me
        </b-button>
        <b-tooltip target="tooltip-target-1" triggers="hover">
          I am tooltip <b>component</b> content!
        </b-tooltip>

        <b-dropdown id="dropdown-1" text="Dropdown Button" class="m-md-2">
          <b-dropdown-item>First Action</b-dropdown-item>
          <b-dropdown-item>Second Action</b-dropdown-item>
          <b-dropdown-item>Third Action</b-dropdown-item>
          <b-dropdown-divider></b-dropdown-divider>
          <b-dropdown-item active>Active action</b-dropdown-item>
          <b-dropdown-item disabled>Disabled action</b-dropdown-item>
        </b-dropdown>
      </div>
      
      <b-table striped hover :items="items" :fields="fields"></b-table>
    </b-card>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      fields: [
        { key: "age", label: "Age", sortable: true },
        { key: "first_name", label: "First Name", sortable: true },
        { key: "last_name", label: "Last Name", sortable: true },
      ],
      items: [
        { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
        { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
        { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
        { age: 38, first_name: 'Jami', last_name: 'Carney' }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.toolbar{
  padding: 4px;
  margin: 4px 20px;
}
.toolbar button{
  margin: 2px;
}
.tableCard{
  margin: 10px;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
