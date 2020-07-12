<template>
  <div class="container">
    <recommend-list :list="recommendList" />
  </div>
</template>

<script>
import RecommendList from '~/components/index/RecommendList'

export default {
  components: {
    RecommendList
  },
  data() {
    return {
      recommendList: [
        {
          thumb:
            'http://img5.imgtn.bdimg.com/it/u=2484758016,2231158131&fm=26&gp=0.jpg',
          title: 'C++',
          desc: '专业职场 课程体系'
        },
        {
          thumb:
            'http://pic1.win4000.com/wallpaper/2017-10-12/59decb9c94d5f.jpg',
          title: 'C++',
          desc: '专业职场 课程体系'
        },
        {
          thumb: 'http://pic1.win4000.com/wallpaper/e/57ca4492a321e.jpg',
          title: 'Python',
          desc: '专业职场 课程体系'
        },
        {
          thumb:
            'http://www.33lc.com/article/UploadPic/2012-8/2012838584578094.jpg',
          title: 'Python',
          desc: '专业职场 课程体系'
        }
      ]
    }
  },
  head() {
    return {
      title: '首页'
    }
  }
}
</script>

<style>
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
