<template>
    <div>
        <!-- 获取普通元素 -->
        <!-- <input type="text" class="form-control" ref="input"> -->
        <!-- 获取列表 -->
        <!-- <ul class="list-group">
            <li class="list-group-item" v-for="(item,index) in list" :key="index"
                ref="list">
                {{item}}
            </li>
        </ul> -->
        <!-- 获取组件 -->
        <!-- <demo-item ref="demoitem"></demo-item> -->

        <!-- $children -->
        <!-- <h1>11111</h1>
        <demo-item></demo-item>
        <demo-item></demo-item> -->

        <!-- $parent -->
        <h1 class="text-center">{{header}}</h1>
        <demo-item></demo-item>
    </div>
</template>

<script>
import demoItem from "./demo-item"
export default {
    data() {
        return {
            header: "我是父组件",
            list: [1,2,3,4,5,6,7,8,9,10]
        }
    },
    components:{
        demoItem
    },
    // 页面渲染完成
    mounted() {
        // 获取input
        // console.log(this.$refs);
        //<input data-v-e06f8548="" type="text" class="form-control" style="border-color: red;">
        // console.log(this.$refs.input);
        // 修改样式
        // this.$refs.input.style.borderColor = 'red';
        // 获取焦点
        // this.$refs.input.focus();

        // 获取列表
        // console.log(this.$refs.list);
        // 随机颜色
        // this.$refs.list.forEach((v) => {
        //     v.style.backgroundColor = '#' + Math.floor(Math.random()*1000000);
        // });
        
        // 获取子组件
        // console.log(this.$refs)
        // 操作子组件方法
        // console.log("父组件操作子组件")
        // this.$refs.demoitem.focus()
        // console.log(this.$refs.demoitem);
        // this.$refs.demoitem.renameHeader("父组件修改子组件");

        // this.$refs.demoitem.val = '父组件修改子组件'

        // console.log(this.$children);
        // this.$children[0].renameHeader('修改第一个');
    },
    methods: {
        // 修改header的值
        parentRename(data) {
            this.header = data;
        }
    }
}
</script>

<style scoped>
    
</style>