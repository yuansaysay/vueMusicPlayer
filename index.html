<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <meta http-equiv="X-UA-Compatible" content="ie=edge"/>
    <title>悦听player</title>
    <!-- 样式 -->
    <link rel="stylesheet" href="./css/index.css">
</head>

<body>
<div class="wrap">
    <!-- 播放器主体区域 -->
    <div class="play_wrap" id="player">
        <div class="search_bar">
            <img src="images/player_title.png" alt=""/>
            <!-- 搜索歌曲 -->
            <input type="text" autocomplete="off" v-model="query" @keyup.enter="searchMusic"/>
        </div>
        <div class="center_con">
            <!-- 搜索歌曲列表 -->
            <div class='song_wrapper'>
                <ul class="song_list">
                    <li v-for="item in musicList">
                        <a href="javascript:;" @click="playMusic(item.id)"></a>
                        <b>{{item.name}}</b>
                        <span v-if="item.mvid!=0" @click="playMovie(item.mvid)"><i></i></span>
                    </li>
                </ul>
                <img src="images/line.png" class="switch_btn" alt="">
            </div>
            <!-- 歌曲信息容器 -->
            <div class="player_con" :class="{playing:isPlaying}">
                <img src="images/player_bar.png" class="play_bar"/>
                <!-- 黑胶碟片 -->
                <img src="images/disc.png" class="disc autoRotate"/>
                <img :src="musicCoverUrl" class="cover autoRotate"/>
            </div>
            <!-- 评论容器 -->
            <div class="comment_wrapper">
                <h5 class='title'>热门留言</h5>
                <div class='comment_list'>
                    <dl v-for="item in hotComments">
                        <dt><img :src="item.user.avatarUrl" alt=""></dt>
                        <dd class="name">{{item.user.nickname}}</dd>
                        <dd class="detail">
                            {{item.content}}
                        </dd>
                    </dl>
                </div>
                <img src="images/line.png" class="right_line">
            </div>
        </div>
        <div class="audio_con">
            <audio ref='audio' @play="play" @pause="pause" :src="musicUrl" controls autoplay loop
                   class="myaudio"></audio>
        </div>
        <div class="video_con" v-show="showVideo">
            <video :src="mvUrl" controls="controls"></video>
            <div class="mask" @click="closeMv"></div>
        </div>
    </div>
</div>
<!-- 开发环境版本，包含了有帮助的命令行警告 -->
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<!-- 官网提供的 axios 在线地址 -->
<script src="https://unpkg.com/axios/dist/axios.min.js"></script>

<script>
    var vm = new Vue({
        el: "#player",
        data: {
            query: "",
            musicList: [],
            musicUrl: "",
            musicCoverUrl: "",
            hotComments: [],
            isPlaying: false,
            showVideo: false,
            mvUrl: "",


        },
        methods: {
            searchMusic() {
                console.log(this.query)
                var that = this;
                axios.get("https://autumnfish.cn/search?keywords=" + that.query).then(
                    function (response) {
                        // console.log(response);
                        that.musicList = response.data.result.songs;
                    },
                    function (err) {
                    }
                );
            },
            playMusic(musicId) {
                var that = this;
                // 获取歌曲
                axios.get("https://autumnfish.cn/song/url?id=" + musicId).then(function (response) {
                        that.musicUrl = response.data.data[0].url;
                    },
                    function (err) {
                    });

                // 歌曲详情获取
                axios.get("https://autumnfish.cn/song/detail?ids=" + musicId).then(
                    function (response) {
                        // console.log(response.data.songs[0].al.picUrl);
                        that.musicCoverUrl = response.data.songs[0].al.picUrl;
                    },
                    function (err) {
                    }
                );

                // 歌曲评论获取
                axios.get("https://autumnfish.cn/comment/hot?type=0&id=" + musicId).then(
                    function (response) {
                        // console.log(response);
                        console.log(response.data.hotComments);
                        that.hotComments = response.data.hotComments;
                    },
                    function (err) {
                    }
                );
            },
            // 歌曲播放
            play: function () {
                // console.log("play");
                this.isPlaying = true;
            },
            // 歌曲暂停
            pause: function () {
                // console.log("pause");
                this.isPlaying = false;
            },
            playMovie(mvid) {
                var that = this;
                that.showVideo = true;
                axios.get("https://autumnfish.cn/mv/url?id=" + mvid).then(
                    function (response) {
                        // console.log(response);
                        console.log(response.data.data.url);
                        that.$refs.audio.pause()
                        that.mvUrl = response.data.data.url;
                    },
                    function (err) {
                    }
                );
            },
            closeMv() {
                this.showVideo = false;
                this.mvUrl = "";
            }
        }
    })

</script>
</body>

</html>
