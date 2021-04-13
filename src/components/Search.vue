<template>
  <ais-instant-search :search-client="searchClient" index-name="demo_ecommerce">
    <ais-search-box />
    <ais-hits>
      <div slot="item" slot-scope="{ item }">
        <h2>{{ item.name }}</h2>
      </div>
    </ais-hits>
  </ais-instant-search>
</template>

<script setup>
import algoliasearch from "algoliasearch/lite";
import "instantsearch.css/themes/satellite-min.css";
import { AisInstantSearch, AisSearchBox, AisHits } from "vue-instantsearch";

const searchClient = algoliasearch(
  "B1G2GM9NG0",
  "aadef574be1f9252bb48d4ea09b5cfe5"
);
</script>
