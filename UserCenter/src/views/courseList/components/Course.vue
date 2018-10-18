<template>
    <div class="courseContainer">
        <div class="courseName">
            高中数学联赛一试课程（18年秋）
        </div>
        <div class="courseNumber">
            总课次数: 12次课
        </div>
        <div class="courseTeachers">
            主讲教师: {{teachers.join('、')}}
        </div>
        <div class="courseTime">
            课程时间: 2018年3月10号起每周六8:00-10:00
        </div>
        <div class="segmentLine"></div>
        <Lecture />
        <!-- <Lecture /> -->
    </div>

</template>

<script>
import Lecture from './Lecture';

export default {
    data() {
        return {
            teachers: ['邹进', '胡小军', '张明宇'],
        };
    },
    components: {
        Lecture,
    },
};
</script>

<style lang="less" scoped>
    @import '../../../assets/reset.less';

    .ellipsis{
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }

    .courseContainer{
        width: 855px;
        height: 340px;
        margin:0 auto 20px;
        box-sizing: border-box;
        padding-top: 25px;
        padding-left: 20px;
        padding-right: 20px;
        background: yellowgreen;
        border: 1px solid #e6e6e6;

        .border-radiuses(5px, 55px, 100px, 5px);
        .courseName{
            .ellipsis;
            font-size: 20px;
            line-height: 20px;
            font-weight: normal;
            color: #333;
            width: 530px;
            text-align: left;
            margin-bottom: 10px;
        }
        .courseNumber, .courseTeachers, .courseTime{
            .ellipsis;
            width: 530px;
            font-size: 14px;
            line-height: 14px;
            text-align: left;
            color: #999;
            margin-bottom: 10px;
            &:nth-of-type(4){
                margin-bottom: 20px;
            }
        }
        .segmentLine{
            width: 100%;
            height: 1px;
            margin-bottom: 20px;
            background: #eee;
        }
        .frame{
            width: 300px;
            background: #ffffff;
        }
    }
</style>

