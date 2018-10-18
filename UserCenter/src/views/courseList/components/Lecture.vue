<template>
    <div class="lectureContainer">
        <div class="lectureLeft block" :class="{isOver: courseStatus === 3}">
            <div class="lectureNumber" >
                <span class="number">
                    2
                </span>
                <span class="word">
                    讲
                </span>
            </div>
            <div class="lectureStatus">
                未开始
            </div>
        </div>
        <div class="lectureRight block">
            <div class="lectureName">
                函数的概念与奇偶性
            </div>
            <div class="rightMiddle">
                <div class="courseTime">
                    2018-10-20 19:00-21:00
                </div>
                <div class="courseTeacher">
                    主讲: 胡小军
                </div>
            </div>
            <div class="lectureReplayButton" :class="{canReplay: courseStatus === 3}">
                <i class="iconfont">&#xe63a;</i>
                <i class="content">直播回顾</i>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            // 1: 未开始  2:正在直播  3:已结束
            courseStatus: 1,
        };
    },
};
</script>

<style lang="less" scoped>
    @font-face {
        font-family: 'iconfont';
        src: url('../iconfont/iconfont.eot');
        src: url('../iconfont/iconfont.eot?#iefix') format('embedded-opentype'),
        url('../iconfont/iconfont.woff') format('woff'),
        url('../iconfont/iconfont.ttf') format('truetype'),
        url('../iconfont/iconfont.svg#iconfont') format('svg');
    }

    .ellipsis{
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }

    .lectureContainer{
        width: 406.5px;
        height: 65px;
        float: left;
        text-align: left;
        background: #fff;
        .block{
            float: left;
        }
        .iconfont{
            font-family:"iconfont" !important;
            font-size:16px;font-style:normal;
            -webkit-font-smoothing: antialiased;
            -webkit-text-stroke-width: 0.2px;
            -moz-osx-font-smoothing: grayscale;
        }
        .lectureLeft{
            width: 55px;
            text-align: center;
            font-size: 12px;
            font-weight: bold;
            color: #FFF;
            background: #c9c9c9;
            margin-right: 20px;
            .lectureNumber{
                font-size: 12px;
                height: 39px;
                line-height: 39px;
                border-bottom: 1px solid #fff;
                .number{
                    font-family: "微软雅黑";
                    font-size: 24px;
                    display: inline-block;
                }
                .word{
                    display: inline-block;
                    margin-left: -3px;
                }
            }
            .lectureStatus{
                height: 25px;
                line-height: 25px;
            }
        }
        .isOver{
            background: #becdd9;
        }
        .lectureRight{
            width: 322px;
            .lectureName{
                font-size: 14px;
                color: #333;
                margin-bottom: 5px;
                .ellipsis;
            }
            .rightMiddle{
                font-size: 12px;
                color: #666;
                margin-bottom: 5px;
                .courseTime, .courseTeacher{
                    display: inline-block;
                    &:first-of-type{
                        margin-right: 15px;
                    }
                }
            }
            .lectureReplayButton{
                font-size: 12px;
                color: #999;
                .iconfont{
                    position: relative;
                    top: 1px;
                }
                .content{
                    position: relative;
                    font-style: normal;
                    left: -3px;
                }
            }
            .canReplay{
                color: #1652ad;
                cursor: pointer;
            }
        }

    }
</style>

