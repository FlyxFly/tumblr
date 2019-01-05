<template>
    <li class="post_wrapper">
        <div class="post_header">
            <div class="post_info" v-show="post.source_title">
                <div class="post_title">
                    <i class="ui icon random"></i>{{post.source_title}}
                </div>
                <a href="#" class="" >关注</a>
            </div>
        </div>
        <div class="post_avatar">
            <div class="post_avatar_wrapper">
                <a href="#" style="background-image: url('https://img.fly2x.com/images/2018/06/15/20173201739522293102411861580_600_0.jpg')"></a>
            </div>
        </div>
        <div class="post_content">
            <div class="photo">
                <img src="https://img.fly2x.com/images/2018/06/15/20173201739522293102411861580_600_0.jpg" class="ui fluid image">
                <div class="text" v-html="post.caption">
                </div>
                
            </div>
            <div class="video">
                
            </div>
            <div class="answer">
                
            </div>
            <div class="text">
                
            </div>
            <div class="quote">
                
            </div>

            <div class="link">
                
            </div>
            <div class="audio">
                
            </div>
        </div>
        <div class="post_footer">
            <span>
                <a class="ui label" :href="post.short_url"><i class="ui icon linkify blue"></i>Source</a>
            </span>
            <span class="right floated">
                <a class="ui label"><i class="ui icon heart outline red"></i>Like</a>
            </span>
        </div>
    </li>  
</template>

<script>
export default {
    name : 'Post',
    props: ['post_data'],
    data:function(){
        return {
            post:this.post_data,
        }
    }
}
</script>

<style scoped>
div.text{
    width: 100%;
    padding:10px;
}



</style>