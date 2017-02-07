<template>
    <div class="tabs">
        <el-tabs v-model="activeName" @tab-click="handleClick">
            <el-tab-pane label="用户管理" name="first">用户管理</el-tab-pane>
            <el-tab-pane label="配置管理" name="second">配置管理</el-tab-pane>
            <el-tab-pane label="角色管理" name="third">角色管理</el-tab-pane>
            <el-tab-pane label="定时任务补偿" name="fourth">定时任务补偿</el-tab-pane>
        </el-tabs>
        <hr>
        <el-tabs v-model="activeName2" type="card" @tab-click="handleClick">
            <el-tab-pane label="用户管理" name="first">用户管理</el-tab-pane>
            <el-tab-pane label="配置管理" name="second">配置管理</el-tab-pane>
            <el-tab-pane label="角色管理" name="third">角色管理</el-tab-pane>
            <el-tab-pane label="定时任务补偿" name="fourth">定时任务补偿</el-tab-pane>
        </el-tabs>
        <hr>
        <el-tabs v-model="activeName3" type="card" closable @tab-click="handleClick" @tab-remove="handleRemove">
            <el-tab-pane label="用户管理">用户管理</el-tab-pane>
            <el-tab-pane label="配置管理">配置管理</el-tab-pane>
            <el-tab-pane label="角色管理">角色管理</el-tab-pane>
            <el-tab-pane label="定时任务补偿">定时任务补偿</el-tab-pane>
        </el-tabs>
        <hr>
        <el-tabs type="border-card">
            <el-tab-pane label="用户管理">用户管理</el-tab-pane>
            <el-tab-pane label="配置管理">配置管理</el-tab-pane>
            <el-tab-pane label="角色管理">角色管理</el-tab-pane>
            <el-tab-pane label="定时任务补偿">定时任务补偿</el-tab-pane>
        </el-tabs>
        <hr>
        <div style="margin-bottom: 20px;">
            <el-button size="small"
                       @click="tabs.push({ name: 'Tab ' +  ++tabIndex, title: 'new Tab', content: 'new Tab content' })">
                add tab
            </el-button>
        </div>
        <el-tabs type="card" closable>
            <el-tab-pane v-for="(item, index) in tabs" :label="item.title" :name="item.name">{{item.content}}
            </el-tab-pane>
        </el-tabs>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                activeName: 'second',
                activeName2: 'third',
                activeName3: 'first',
                tabIndex: 0,
                tabs: [
                    {name: 'Tab one', title: 'new Tab', content: 'new Tab content'}
                ]
            };
        },
        methods: {
            handleRemove(tab) {
                console.log(tab);
            },
            handleClick(tab, event) {
                console.log(tab, event);
            }
        }
    };
</script>
<style>

</style>