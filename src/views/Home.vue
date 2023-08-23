<template>
    <div class="card col-md-8  offset-md-1 col-xs-12">
        <div class="article_class col-xs-12 col-md-12">
            <ul class="col-xs-12">


                <li class="col-md-1 col-xs-3 " :class="{ active: activeTab === 'latest' }" @click="changeStyle('latest')">最新文章</li>
                <li class="col-md-1 col-xs-3" :class="{ active: activeTab === 'popular' }" @click="changeStyle('popular')">热门文章</li>
                <li class="col-md-1 col-xs-3" :class="{ active: activeTab === 'most_comments' }" @click="changeStyle('most_comments')">
                    评论最多</li>
                <li class="col-md-1 col-xs-3" :class="{ active: activeTab === 'most_likes' }" @click="changeStyle('most_likes')">点赞最多
                </li>
            </ul>
        </div>
        <div class="card-body">


            <ArticleItem></ArticleItem>
            <ArticleItem></ArticleItem>
            <ArticleItem></ArticleItem>
            <ArticleItem></ArticleItem>
        </div>
    </div>
</template>



<script>
import ArticleItem from '../components/ArticleItem.vue';
export default {
    components: {
        ArticleItem
    },
    data() {
        return {
            activeTab: 'latest',

        }
    },
    methods: {
        changeStyle(tabName) {
            this.activeTab = tabName;
        }

    },

}


</script>



<style scoped>
.card {
    /* width: 60vw; */
    margin-top: 3vh;


}

.article_class li {
    list-style: none;
    text-align: center;
    cursor: pointer;
    color: rgb(111, 113, 116);
}

.article_class ul {
    display: flex;

}

.active {
    border-bottom: 3px solid rgb(78, 165, 255);
    color: rgb(78, 165, 255);
}
.article_class{
    border-bottom: 1px solid rgb(235, 238, 245);
   
}
@media screen and (max-width: 600px) { /*当屏幕尺寸小于600px时，应用下面的CSS样式*/
    .article_class ul {
    display: flex;
    justify-content: space-around;

}
  }
</style>