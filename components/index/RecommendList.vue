<template>
  <div class="recommend-list">
    <div v-for="(item, index) in list" :key="index" class="recommend-list-item">
      <div class="recommend-list-item__inner">
        <div
          class="recommend-list-item__thumb"
          :style="{ backgroundImage: `url(${item.thumb})` }"
        />
        <div class="recommend-list-item__content">
          <h4 class="recommend-list-item__title">{{ item.title }}</h4>
          <p class="recommend-list-item__desc">{{ item.desc }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    list: {
      type: Array,
      default() {
        return []
      }
    }
  }
}
</script>

<style lang="less" scoped>
.recommend-list {
  display: flex;
  padding: 30px 0;
  margin-left: -5px;
  margin-right: -5px;

  &-item {
    flex: 1;
    padding: 0 5px;

    &__inner {
      cursor: pointer;
      height: 249px;
      background-color: #ffffff;
      border-radius: 10px;
      overflow: hidden;
      position: relative;
    }

    &__content {
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      width: 100%;
      height: 100%;
      line-height: 1;
      color: #ffffff;
      padding: 18px;
      background: linear-gradient(
        0deg,
        rgba(3, 0, 0, 0.7) 0%,
        rgba(255, 255, 255, 1) 100%
      );
      position: absolute;
      top: 0;
      left: 0;

      &:hover {
        background: none;
      }
    }

    &__thumb {
      height: 100%;
      background-size: cover;
      background-position: center;
    }

    &__title {
      font-size: 40px;
      font-weight: normal;
      margin-bottom: 15px;
    }

    &__desc {
      font-size: 19px;
    }
  }
}
</style>
