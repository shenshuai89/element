<template>
    <div id="rate">
        <div class="block">
            <span class="demonstration">默认不区分颜色</span>
            <el-rate v-model="value1"></el-rate>
        </div>
        <div class="block">
            <span class="demonstration">区分颜色</span>
            <el-rate
                    v-model="value2"
                    :colors="['#99A9BF', '#F7BA2A', '#FF9900']">
            </el-rate>
        </div>
        <div class="block">
            <span class="demonstration">辅助文字</span>
            <el-rate
                    v-model="value3"
                    show-text>
            </el-rate>
        </div>
        <div class="block">
            <span class="demonstration">只读</span>
            <el-rate
                    v-model="value5"
                    disabled
                    show-text
                    text-color="#ff9900"
                    text-template="{value}">
            </el-rate>
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                value1: null,
                value2: null,
                value3: null,
                value4: null,
                value5: 3.6
            }
        }
    }
</script>
<style scoped>

</style>