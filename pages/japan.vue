<script>
export default {
  asyncData({ params }) {
    return {
      score: require("~/datas/GlobalGenderGapReport2020/Japan/json/Japan-Score.json"),
      summary: require("~/datas/GlobalGenderGapReport2020/Japan/json/Japan-Summary.json"),
    }
  }
}
</script>

<template>
  <main>
    <article class="content" v-html="score"></article>
    <article class="content" v-html="summary"></article>
  </main>
</template>
