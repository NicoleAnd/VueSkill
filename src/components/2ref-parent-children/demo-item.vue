<template>
    <div>
        <h2>{{header}}</h2>
        <input type="text" class="form-control" v-model="val" 
            ref="input" @input="changeInput">
    </div>
</template>
<script>
export default {
    data() {
        return {
            header: "标题header",
            val: '输入框内容'
        }
    },
    methods: {
        focus() {
            this.$refs.input.focus()
        },
        renameHeader(data) {
            this.header = data;
        },
        // changeInput(e) {
        //     console.log(e.target.value);
        //     // 修改父组件的header内容
        //     this.$parent.header = e.target.value;
        // }

        changeInput(e) {
            // console.log(e.target.value);
            // 修改父组件的header内容，修改父组件data下header的值
            // this.$parent.header = e.target.value;
            // 修改父组件的header内容，调用父组件methods的parentRename方法去修改header的值
            this.$parent.parentRename(e.target.value);
        }
    }
}
</script>
<style scoped>
    
</style>