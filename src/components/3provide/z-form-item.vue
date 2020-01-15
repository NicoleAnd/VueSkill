<template>
    <div class="form-group">
        <label :for="name">{{label}}</label>
        <slot />
        <div class="valid-feedback">用户名不能为空</div>
    </div>
</template>
<script>
export default {
    props: ['label','name'],
    // 接收父组件注入的属性
    inject: ['form','validate'],
    data() {
        return {
            valis: {}
        }
    },
    // 页面渲染完成后
    mounted() {
        // 初始化验证规则
        this.validate.forEach((v) => {
            console.log(v);
            if(v.name === this.name){
                this.valis = v.validate
            }
        });
        // 开启监听器，监听字段变化
        this.$watch(`form.${this.name}`,(newValue,oldValue)=>{
            console.log(newValue)
            // 验证数据是否合法
            // 1.验证是否必填
            if(this.valis.required.data){
                if(newValue === '') {
                    console.log(this.valis.required.msg)
                    return
                }
            }
            // 2.验证其他规则

        })
    }
}
</script>
<style>
    
</style>