<template>
  <ais-instant-search :search-client="searchClient" index-name="demo_ecommerce">
    <!-- <ais-configure :hits-per-page="4" /> -->
    <ais-search-box />
    <ais-hits>
      <template v-slot:item="{ item }">
        <div>
          <h2>{{ item.name }}</h2>
        </div>
      </template>
    </ais-hits>
    <ais-pagination />
  </ais-instant-search>
</template>

<script setup>
import algoliasearch from "algoliasearch/lite";
import "instantsearch.css/themes/satellite-min.css";
import {
  AisInstantSearch,
  AisConfigure,
  AisPagination,
  AisSearchBox,
  AisHits,
} from "vue-instantsearch";

const searchClient = algoliasearch(
  "B1G2GM9NG0",
  "aadef574be1f9252bb48d4ea09b5cfe5"
);
</script>
