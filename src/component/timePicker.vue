<template>
    <div id="timePicker">
        <el-time-picker
            v-model="value1"
            :picker-options="{
              selectableRange: '09:00:00 - 18:00:00'
            }"
            size="large"
            placeholder="任意时间点">
        </el-time-picker>
        <el-time-select
            placeholder="起始时间"
            v-model="startTime"
            size="small"
            :picker-options="{
              start: '08:30',
              step: '00:15',
              end: '18:30'
            }">
        </el-time-select>
        <el-time-select
            placeholder="结束时间"
            v-model="endTime"
            :picker-options="{
              start: '08:30',
              step: '00:15',
              end: '18:30',
              minTime: startTime
            }">
        </el-time-select>
        <el-time-picker
                is-range
                v-model="value2"
                placeholder="选择时间范围">
        </el-time-picker>
    </div>
</template>
<script>
    export default{
        data() {
            return {
                value1: new Date(2016, 9, 10, 12, 30),
                startTime: '',
                endTime: '',
                value2: [new Date(2016, 9, 10, 8, 40), new Date(2016, 9, 10, 9, 40)]
            };
        }
    }
</script>
<style scoped>

</style>