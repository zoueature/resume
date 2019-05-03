<template>
    <div class="experience">
        <div class="skill experience-list">
            <div class="item-title">
                <span><b>自我评价</b></span>
            </div>
            {{name}}
        </div>
        <div class="projects">
            {{email}}
        </div>
        <div class="work-experience">
            {{github}}
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
        name: "Experience"
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
        margin: 10px auto;
    }
</style>