<template>
    <div class="demo">
        <h2>学生姓名:{{studentName}}</h2>
        <h2>学生地址:{{studentAddress}}</h2>
        <button @click="showName">点我显示学生名</button>
    </div>
</template>

<script>
    // 3种暴露方式
    // 1.分别暴露
    export default {
        name: 'StudentHello',
        // 不用写el配置项 因为所有的组件都要被一个vm管理
        data() { // 每次调用返回一个全新的对象
            return {
                studentName: "张三",
                studentAddress: "18"
            }
        },
        methods: {
            showName() {
                alert(this.studentName)
            }
        }
    }
    // 2. 统一暴露
    //export {student}

    // 3.默认暴露 常用
    // export default student
</script>

<style>
    /*    组件的样式 */
    .demo {
        background-color: aquamarine;
    }
</style>

