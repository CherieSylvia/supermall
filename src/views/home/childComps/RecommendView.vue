<template>
    <div class="recommend">
      <div v-for="(item,index) in recommends" :key="index" class="recommendItem">
        <a :href="item.link">
          <img :src="item.image" alt="">
          <div>{{ item.title }}</div>
        </a>
      </div>
    </div>
</template>

<script>
  export default {
    name: "RecommendView",
    props: {
      recommends: {
        type: Array,
        default() {
          return [];
        }
      }
    }
  }
</script>

<style scoped>
  .recommend {
    display: flex;
    width: 100%;
    text-align: center;
    font-size: 12px;
    padding: 15px 0 30px;
    border-bottom: 10px solid #eee;
  }
  .recommendItem {
    flex: 1;
  }
  .recommendItem img {
    width: 90%;
    margin-bottom: 10px;
  }
</style>
