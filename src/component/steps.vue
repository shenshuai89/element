<template>
    <div id="steps">
        <el-steps :space="100" :active="active" finish-status="success">
            <el-step title="步骤 1"></el-step>
            <el-step title="步骤 2"></el-step>
            <el-step title="步骤 3"></el-step>
        </el-steps>

        <el-button style="margin-top: 12px;" @click="next">下一步</el-button>
        <hr>
        <el-steps :space="100" :active="active1" finish-status="success">
            <el-step title="已完成"></el-step>
            <el-step title="进行中"></el-step>
            <el-step title="步骤 3"></el-step>
        </el-steps>
        <el-button style="margin-top: 12px;" @click="nextTwo">下一步</el-button>
        <hr>
        <el-steps :space="100" :active="active2" >
            <el-step title="步骤 1" icon="edit"></el-step>
            <el-step title="步骤 2" icon="upload"></el-step>
            <el-step title="步骤 3" icon="picture"></el-step>
        </el-steps>
        <el-button style="margin-top: 12px;" @click="nextThree">下一步</el-button>
        <hr>
        <el-steps :space="100" direction="vertical" :active="active3">
            <el-step title="步骤 1"></el-step>
            <el-step title="步骤 2"></el-step>
            <el-step title="步骤 3"></el-step>
        </el-steps>
        <el-button style="margin-top: 12px;" @click="nextFour">下一步</el-button>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                active: 0,
                active1: 1,
                active2: 1,
                active3: 1
            };
        },
        methods: {
            next() {
                if (this.active++ > 2) this.active = 0;
            },
            nextTwo() {
                if (this.active1++ > 2) this.active1 = 0;
            },
            nextThree() {
                if (this.active2++ > 2) this.active2 = 0;
            },
            nextFour() {
                if (this.active3++ > 2) this.active3 = 0;
            }
        }
    }
</script>
<style>
#steps{
    margin-top: 20px;
}
</style>