<template>
    <div id="checkbox">
            <el-checkbox-group v-model="checkList">
                <el-checkbox label="复选框 A"></el-checkbox>
                <el-checkbox label="复选框 B"></el-checkbox>
                <el-checkbox label="复选框 C"></el-checkbox>
                <el-checkbox label="禁用" disabled></el-checkbox>
                <el-checkbox label="选中且禁用" disabled></el-checkbox>
            </el-checkbox-group>
        <div style="margin-top:10px;"></div>
            <el-checkbox :indeterminate="isIndeterminate" v-model="checkAll" @change="handleCheckAllChange">全选</el-checkbox>
            <div style="margin: 15px 0;"></div>
            <el-checkbox-group v-model="checkedCities" @change="handleCheckedCitiesChange">
                <el-checkbox v-for="city in cities" :label="city">{{city}}</el-checkbox>
            </el-checkbox-group>
    </div>
</template>
<script>
    const cityOptions = ['上海', '北京', '广州', '深圳'];
    export default{
        data() {

            return {
                checkList: ['选中且禁用', '复选框 A'],
                checkAll: true,
                checkedCities: [],
                cities: cityOptions,
                isIndeterminate: false
            };
        },
        methods: {
            handleCheckAllChange(event) {
                this.checkedCities = event.target.checked ? cityOptions : [];
                this.isIndeterminate = false;
            },
            handleCheckedCitiesChange(value) {
                let checkedCount = value.length;
                this.checkAll = checkedCount === this.cities.length;
                this.isIndeterminate = checkedCount > 0 && checkedCount < this.cities.length;
            }
        }
    }
</script>
<style scoped>
    #checkbox {
        margin-top: 10px;
    }
</style>