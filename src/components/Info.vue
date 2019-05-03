<template>
    <div class="info">
        <div class="basic-info">
            <div class="avatar">
                <img v-bind:src="avatar" v-bind:alt="name" width="100%" height="100%">
            </div>
            <div class="name">
                <b>姓名</b>： {{name}}
            </div>
            <div class="email">
                <b>邮箱</b>： <a v-bind:href="emailTo" title="zoueature@gmail.com">{{email}}</a>
            </div>
            <div class="edu">
                <b>毕业院校</b>： {{edu}}-{{profession}}
            </div>
            <div class="grad">
                <b>毕业时间</b>： {{graduationDate}}
            </div>
            <div class="github">
                <b>GitHub</b>： <a v-bind:href="github" title="zoueature" target="_blank">{{github}}</a>
            </div>
        </div>
        <div class="skill-bar-info">
            <div class="item-title">
                <span><b>技能掌握</b></span>
            </div>
            <div v-for="skill in skills">
                <div class="skill-bar">
                    <div class="bar-name">
                        {{skill.name}}
                    </div>
                    <div class="bar-back" :style="{backgroundColor:skill.backColor}">
                        <div class="bar-front" :style="{backgroundColor:skill.frontColor, width: skill.process}">
                            <span style="float: right; line-height: 150%; font-size: 13px;">{{skill.process}}</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="intro-myself">
            <div class="item-title">
                <span><b>自我评价</b></span>
            </div>
            <div v-for="item in intro">
                <ul class="intro-list">
                    <li>{{item}}</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Info",
        data: function () {
            return {
                avatar: "https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=590506442,2441509563&fm=26&gp=0.jpg",
                name: "Eature",
                email: "zoueature@gmail.com",
                emailTo: "mailto:zoueature@gmail.com",
                github: "https://github.com/eaturezou",
                edu: "集美大学",
                profession: "网络工程",
                graduationDate: "2017-07",
                skills: [
                    {
                        name: "PHP", //技能名
                        backColor: "#dcdcdc", //背景颜色
                        frontColor: "#12E2FF", //前景颜色
                        process: "90%" //前景进度条
                    },
                    {
                        name: "Linux", //技能名
                        backColor: "#dcdcdc", //背景颜色
                        frontColor: "#41ff0b", //前景颜色
                        process: "75%" //前景进度条
                    },
                    {
                        name: "MySQL", //技能名
                        backColor: "#dcdcdc", //背景颜色
                        frontColor: "#ff1624", //前景颜色
                        process: "75%" //前景进度条
                    },
                    {
                        name: "NoSQL", //技能名
                        backColor: "#dcdcdc", //背景颜色
                        frontColor: "#325fff", //前景颜色
                        process: "70%" //前景进度条
                    },
                    {
                        name: "HTML", //技能名
                        backColor: "#dcdcdc", //背景颜色
                        frontColor: "#ffd72a", //前景颜色
                        process: "60%" //前景进度条
                    },
                    {
                        name: "JS", //技能名
                        backColor: "#dcdcdc", //背景颜色
                        frontColor: "#fd48ff", //前景颜色
                        process: "60%" //前景进度条
                    },
                    {
                        name: "CSS", //技能名
                        backColor: "#dcdcdc", //背景颜色
                        frontColor: "#6811ff", //前景颜色
                        process: "55%" //前景进度条
                    }
                ],
                intro: [
                    "优秀的学习能力,对新事物始终保持好奇心,对新事物始终保持好奇心",
                    "对新事物始终保持好奇心",
                    "优秀的学习能力",
                    "对新事物始终保持好奇心",
                    "优秀的学习能力",
                    "对新事物始终保持好奇心"
                ],

            }
        }
    }
</script>

<style scoped>
    a {
        text-decoration: none;
        color: #007cec;
    }
    .info {
        width: 35%;
        height: 100%;
        background-color: #f0f0f0;
        float: right;
        overflow: hidden;
        position: absolute;
        right: 0;
        top: 0;
    }
    .avatar {
        width: 120px;
        height: 120px;
        overflow: hidden;
        border-radius: 50%;
        left: 0;
        right: 0;
        margin: 25px auto;

    }
    .name, .email, .github, .edu, .grad {
        animation-name: flyLeft;
        animation-duration: 1500ms;
        position: relative;
        margin-top: 25px;
        margin-left: 5%;
    }
    .email {
        animation-duration: 1350ms;
    }
    .edu {
        animation-duration: 1200ms;
    }
    .grad {
        animation-duration: 1050ms;
    }
    .github {
        animation-duration: 900ms;
    }
    .skill-bar-info {
        width: 97%;
        margin: 27px auto;
    }
    .skill-bar {
        width: 100%;
        height: 22px;
        margin-top: 20px;
    }
    .bar-name {
        float: left;
        width: 18%;
        height: 100%;
        text-align: center;
        font-size: 13px;
        line-height: 150%;
        overflow: hidden;
        font-weight: bold;
        color: #444444;
    }
    .bar-back {
        float: left;
        width: 80%;
        height: 100%;
        margin-left: 2%;
    }
    .bar-front {
        float: left;
        height: 100%;
        border-radius: 0 11px 11px 0;
        animation-duration: 1s;
        animation-name: processUp;
    }
    .intro-myself {
        width: 97%;
        margin: 27px auto;
    }
    .intro-list {
        list-style-type: square;
        font-size: 13px;
        color: #222222;
    }
    .intro-list li {
        margin-top: -10px;
    }
</style>