<template>
    <b-container>
      <h1 class="text-center pt-5">Каталог товаров</h1>
      <hr>
      <b-row>
        <b-col sm="3">
          <div class="filters">
          <CatalogFilter/>
          </div>
        </b-col>
        <b-col sm="9">
          sggfgsdgsdgwegweg
        </b-col>
      </b-row>
    </b-container>
</template>

<script>
    import CatalogFilter from "../components/CatalogFilter";
    export default {
        name: "catalog",
      components: {CatalogFilter}
    }
</script>

<style scoped>
  .filters {
    border-right: 1px solid lightgrey;
  }

</style>
