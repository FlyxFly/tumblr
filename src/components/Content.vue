<template>
    <div class="k_content ui container" id="k_content">
        <div class="k_right_column">
            <div class="k_keywords">
                <div class="h4">#keyword</div>
                <div class="actions">
                    <a href="">清除搜索</a>
                </div>
            </div>
            <div class="divider"></div>
            RECOMMENDED BLOGS
            <div class="divider"></div>
        </div>
        <div class="k_left_column">
            <ul>
                <Post v-for="post in posts" :post_data="post" :key="post.id"></Post>
            </ul>
        </div>
    </div>
</template>
<script>
import Post from './Post'
export default {
    name:'Content',
    props:['posts_data'],
    components:{Post},
    data:function(){
        return {
            posts:this.posts_data
        }
    },
    mounted:function(){
        let self=this;
        this.$nextTick(function(){
        })
    }
}
</script>