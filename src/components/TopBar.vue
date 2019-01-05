<template>
    <div class="ui inverted menu" id="k_header">
        <div class="ui container" id="k_header_container">
            <div class="header item"><i class="icon large tumblr"></i></div>
            <div class="item">
                <div class="ui transparent inverted icon input">
                    <i class="search icon"></i>
                    <input type="text" placeholder="Search">
                </div>
            </div>
            <div class="right menu">
                <a class="item"><i class="icon large home"></i></a>
                <a class="item"><i class="icon large compass"></i></a>
                <a class="item"><i class="icon large mail"></i></a>
                <a class="item"><i class="icon large send"></i></a>
                <a class="item"><i class="icon large announcement"></i></a>
                <a class="item"><i class="icon large user"></i></a>
                <a class="item"><i class="icon large write"></i></a>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        name:'TopBar'
    }
</script>