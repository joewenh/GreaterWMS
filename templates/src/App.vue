<template>
  <div id="q-app">
    <router-view />
  </div>
</template>
<style lang="sass">
.my-sticky-header-column-table
  /* height or max-height is important */

  /* specifying max-width so the example can
    highlight the sticky column on any browser window */

  td:last-child
    /* bg color is important for td; just specify one */
    background-color: $grey-1 !important
  tr th
    position: sticky
    /* higher than z-index for td below */
    z-index: 2
    /* bg color is important; just specify one */
    background: white
  /* this will be the loading indicator */
  thead tr:last-child th
    /* height of all previous header rows */
    top: 48px
    /* highest z-index */
    z-index: 3
  thead tr:first-child th
    top: 0
    z-index: 1
  tr:first-child th:first-child
    /* highest z-index */
    z-index: 3
  td:first-child
    z-index: 1
  td:last-child, th:last-child
    position: sticky
    right: 0
</style>
<style lang="sass">
.my-sticky-header-table
  /* height or max-height is important */

  .q-table__top,
  .q-table__bottom,
  thead tr:first-child th
    /* bg color is important for th; just specify one */
    background-color: white
  thead tr th
    position: sticky
    z-index: 1
  thead tr:first-child th
    top: 0
  /* this is when the loading indicator appears */
  &.q-table--loading thead tr:last-child th
    /* height of all previous header rows */
    top: 48px
</style>
<script >
export default {
  name: 'App'
}
</script>
