<template>
    <div class="experience">
        <div class="skill experience-list">
            <div class="item-title">
                <span><b>专业技能掌握</b></span>
            </div>
            <div v-for="skill in skills" class="skill-list">
                <div class="skill-name">
                    {{skill.name}}
                </div>
                <div class="skill-description">
                    {{skill.description}}
                </div>
                <div style="clear: both;"></div>
            </div>
        </div>
        <div class="projects experience-list">
            <div class="item-title">
                <span><b>项目经历</b></span>
            </div>
            <div v-for="project in projects" class="project-list">
                <div class="project-title">
                    <div class="project-name">
                        {{project.name}}
                    </div>
                    <div class="project-time">
                        {{project.time}}
                    </div>
                    <div class="project-url">
                        <a :href="project.github" :title="project.github">{{project.github}}</a>
                    </div>
                </div>
                <div style="clear: both;"></div>
                <div class="project-content">
                    <div class="project-tags">
                        <div class="tag-item" v-for="tag in project.tag">
                            {{tag}}
                        </div>
                    </div>
                    <div class="project-desc">
                        {{project.description}}
                    </div>
                    <div style="clear: both;"></div>
                </div>
            </div>
        </div>
        <div class="work-experience experience-list">
            <div class="item-title">
                <span><b>工作经历</b></span>
            </div>
        </div>
        <div class="edu-experience">
            {{edu}}
        </div>
        <div class="grad">
            {{graduationDate}}
        </div>
    </div>
</template>

<script>
    export default {
        name: "Experience",
        data: function () {
            return {
                skills: [
                    {
                        name: "PHP",
                        description: "如果你需要基于环境有条件地配置行为，或者想要直接修改配置，那就换成一个函数 (该函数会在环境变量被设置之后懒执行)。该方法的第一个参数会收到已经"
                    },
                    {
                        name: "Linux",
                        description: "第一个参数会收到已经解析好的配置。在函数内，你可以直接修改配置，或者返回一个将会被合并的对"
                    },
                    {
                        name: "DataBase",
                        description: "当你构建一个 Web Components 组件包的时候，你也可以使用一个 glob 表达式作为入口指定多个组件目标"
                    },
                    {
                        name: "前端",
                        description: "它允许我们更细粒度的控制其内部配置。接下来有一些常见的在 vue.config.js 中的 chainWebpack 修改的例子。"
                    },
                    {
                        name: "框架",
                        description: "对于 CSS 相关 loader 来说，我们推荐使用 css.loaderOptions 而不是直接链式指定 loader。这是因为每种 CSS 文件类型都有多个规则，而 css.loaderOptions"
                    },
                    {
                        name: "Go",
                        description: "\n" +
                            "因为 @vue/cli-service 对 webpack 配置进行了抽象，所以理解配置中包含的东西会比较困难，尤其是当你打算自行对其调整的时候。\n" +
                            "\n" +
                            "vue-cli-service 暴露了 inspect 命令用于审查解析好的 webpack 配置。那个全局的 vue 可执行程序同样提供了 inspect 命令，这个命令只是简单的把 vue-cli-service inspect 代理到了你的项目中。"
                    }
                ],
                projects: [
                    {
                        "name": "12306抢票",
                        "github": "https://github.com/eaturezou/jdi",
                        "time": "2019/07",
                        "description": "有些外部工具可能需要通过一个文件访问解析好的 webpack 配置，比如那些需要提供 webpack 配置路径的 IDE 或 CLI。在这种情况下你可以使用如下路径：",
                        "tag": [
                            "PHP",
                            "MySQL",
                            "JavaScript",
                            "Css"
                        ]
                    },
                    {
                        "name": "12306抢票",
                        "github": "https://github.com/eaturezou/jdi",
                        "time": "2019/07",
                        "description": "有些外部工具可能需要通过一个文件访问解析好的 webpack 配置，比如那些需要提供 webpack 配置路径的 IDE 或 CLI。在这种情况下你可以使用如下路径：",
                        "tag": [
                            "PHP",
                            "MySQL",
                            "JavaScript",
                            "Css"
                        ]
                    },
                    {
                        "name": "12306抢票",
                        "github": "https://github.com/eaturezou/jdi",
                        "time": "2019/07",
                        "description": "有些外部工具可能需要通过一个文件访问解析好的 webpack 配置，比如那些需要提供 webpack 配置路径的 IDE 或 CLI。在这种情况下你可以使用如下路径：",
                        "tag": [
                            "PHP",
                            "MySQL",
                            "JavaScript",
                            "Css"
                        ]
                    },
                    {
                        "name": "12306抢票",
                        "github": "https://github.com/eaturezou/jdi",
                        "time": "2019/07",
                        "description": "有些外部工具可能需要通过一个文件访问解析好的 webpack 配置，比如那些需要提供 webpack 配置路径的 IDE 或 CLI。在这种情况下你可以使用如下路径：",
                        "tag": [
                            "PHP",
                            "MySQL",
                            "JavaScript",
                            "Css"
                        ]
                    },
                    {
                        "name": "12306抢票",
                        "github": "https://github.com/eaturezou/jdi",
                        "time": "2019/07",
                        "description": "有些外部工具可能需要通过一个文件访问解析好的 webpack 配置，比如那些需要提供 webpack 配置路径的 IDE 或 CLI。在这种情况下你可以使用如下路径：",
                        "tag": [
                            "PHP",
                            "MySQL",
                            "JavaScript",
                            "Css"
                        ]
                    }
                ]
            }
        }
    }
</script>

<style scoped>
    .experience {
        width: 64.5%;
        height: 100%;
        position: absolute;
        background-color: #f0f0f0;
        left: 0;
    }
    .experience-list {
        width: 96%;
        margin: 7px auto;
        background-color: #ececec;
        padding: 7px 0;
    }
    .skill-list {
        width: 96%;
        margin: 7px auto;
    }
    .skill-name {
        float: left;
        width: 15%;
        font-weight: bold;
        font-size: 15px;
        color: #333333;
    }
    .skill-description {
        float: left;
        width: 85%;
        font-size: 13px;
        color: #555555;
    }
    .project-list {
        border-top: 5px solid #FFFFFF;
        padding-bottom: 7px;
    }
    .project-title {
        width: 100%;
        height: 30px;
        text-align: center;
    }
    .project-name {
        width: 30%;
        height: 100%;
        float: left;
        font-size: 15px;
        font-weight: bold;
        text-align: center;
        line-height: 200%;
    }
    .project-time {
        width: 20%;
        height: 100%;
        float: left;
        line-height: 200%;
        vertical-align:middle
    }
    .project-url {
        width: 50%;
        height: 100%;
        float: left;
        line-height: 200%;
    }
    .project-content {
        width: 100%;
    }
    .project-tags {
        width: 25%;
        float: left;
    }
    .tag-item {
        float: left;
        border: 1px solid #00c2c3;
        border-radius: 20px;
        text-align: center;
        padding: 1px 4px 1px 4px;
        margin-left: 10px;
        font-size: 12px;
        color: #555555;
        background-color: #ffffff;
        margin-top: 5px;
    }
    .tag-item:nth-child(odd) {
        margin-left: 0;
    }
    .project-desc {
        width: 75%;
        float: left;
        text-indent: 20px;
        font-size: 13px;
        color: #333333;
    }
</style>