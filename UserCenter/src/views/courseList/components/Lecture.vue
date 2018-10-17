<template>
    <div class="lectureContainer">
        <div class="lectureLeft block">
            <div class="lectureNumber">
                <span class="number">
                    1
                </span>
                讲
            </div>
            <div class="lectureStatus">
                未开始
            </div>
        </div>
        <div class="lectureRight block">
            <div class="lectureName">
                函数的概念与奇偶性
            </div>
        </div>
    </div>
</template>

<script>
export default {

};
</script>

<style lang="less" scoped>
    .lectureContainer{
        width: 406.5px;
        height: 65px;
        float: left;
        text-align: left;
        // background: orangered;
        .block{
            display: inline-block;
        }
        .lectureLeft{
            width: 55px;
            height: 39px;
            font-size: 12px;
            color: #FFF;
            background: #EEE;
        }
    }
</style>

