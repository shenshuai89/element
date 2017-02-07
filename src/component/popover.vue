<template>
    <div class="popover">
        <el-popover
                ref="popover1"
                placement="top-start"
                title="标题"
                width="200"
                trigger="hover"
                content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
        </el-popover>

        <el-popover
                ref="popover2"
                placement="bottom"
                title="标题"
                width="200"
                trigger="click"
                content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
        </el-popover>

        <el-button v-popover:popover1>hover 激活</el-button>
        <el-button v-popover:popover2>click 激活</el-button>
        <el-popover
                placement="right"
                title="标题"
                width="200"
                trigger="focus"
                content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
            <el-button slot="reference">focus 激活</el-button>
        </el-popover>
        <hr>
        <el-popover
                ref="popover5"
                placement="top"
                width="160"
                v-model="visible2">
            <p>这是一段内容这是一段内容确定删除吗？</p>
            <div style="text-align: right; margin: 0">
                <el-button size="mini" type="text" @click="visible2 = false">取消</el-button>
                <el-button type="primary" size="mini" @click="visible2 = false">确定</el-button>
            </div>
        </el-popover>

        <el-button v-popover:popover5>删除</el-button>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                visible2: false,
            };
        }
    }
</script>