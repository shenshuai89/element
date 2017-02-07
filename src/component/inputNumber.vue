<template>
    <div id="inputNumber">
        <el-input-number size="large" v-model="num4"></el-input-number>
        <el-input-number v-model="num5"></el-input-number>
        <el-input-number size="small" v-model="num6"></el-input-number>
        <div style="margin-top:10px;">
            <el-input-number v-model="num3" :step="2"></el-input-number>
        </div>
    </div>
</template>
<script>
    export default{
        data() {
            return {
                num3: 5,
                num4: 1,
                num5: 1,
                num6: 1
            }
        }
    }
</script>
<style scoped>
    #inputNumber {
        margin-top: 10px;
    }
</style>