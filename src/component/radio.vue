<template>
    <div id="radio">
        <el-radio class="radio" v-model="radio" label="1">单选项a</el-radio>
        <el-radio class="radio" v-model="radio" label="2">单选项b</el-radio>
        <div style="margin: 15px 0;"></div>
        <el-radio-group v-model="radio3">
            <el-radio-button label="上海"></el-radio-button>
            <el-radio-button label="北京"></el-radio-button>
            <el-radio-button label="广州"></el-radio-button>
            <el-radio-button label="深圳"></el-radio-button>
        </el-radio-group>
        <div style="margin: 15px 0;"></div>
        <el-radio-group v-model="radio4">
            <el-radio-button label="上海"></el-radio-button>
            <el-radio-button label="北京" :disabled="true"></el-radio-button>
            <el-radio-button label="广州"></el-radio-button>
            <el-radio-button label="深圳"></el-radio-button>
        </el-radio-group>
        <div style="margin: 15px 0;"></div>
        <el-radio-group v-model="radio5" :disabled="true">
            <el-radio-button label="上海"></el-radio-button>
            <el-radio-button label="北京"></el-radio-button>
            <el-radio-button label="广州"></el-radio-button>
            <el-radio-button label="深圳"></el-radio-button>
        </el-radio-group>
    </div>
</template>

<script>
    export default {
        data () {
            return {
                radio: '1',
                radio3: '上海',
                radio4: '上海',
                radio5: '上海'
            };
        }
    }
</script>

<style scoped>
    #radio {
        margin-top: 10px;
    }
</style>