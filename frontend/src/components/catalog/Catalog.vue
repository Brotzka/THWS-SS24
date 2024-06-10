<template>
    <div>
        <ais-instant-search :search-client="searchClient" index-name="products">

            <ais-dynamic-widgets>
                <ais-refinement-list attribute="categories" :show-more="true" />
            </ais-dynamic-widgets>

            <ais-hits>
                <template v-slot:item="{item}">
                    <h2>{{ item.name }}</h2>
                </template>
            </ais-hits>
        </ais-instant-search>
    </div>
</template>

<script setup>
import algoliasearch from 'algoliasearch/lite'
import 'instantsearch.css/themes/algolia-min.css'

const searchClient = algoliasearch(
    '42ASY60BGE',
    '924ec83ace068ea172eac93f844ee954'
)

</script>

<style scoped>
body {
  font-family: sans-serif;
  padding: 1em;
}
</style>