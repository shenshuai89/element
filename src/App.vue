<template>
    <div id="app">
        <img src="./assets/logo.png" width="50" height="50">
        <h1>{{ msg }}</h1>
        <el-button @click.native="startHacking">Let's do it</el-button>
        <layout></layout>
        <icon></icon>
        <btn></btn>
        <radio></radio>
        <checkbox></checkbox>
        <el-input></el-input>
        <input-number></input-number>
        <el-select></el-select>
        <el-switch></el-switch>
        <slider></slider>
        <time-picker></time-picker>
        <date-picker></date-picker>
        <date-time-picker></date-time-picker>
        <upload></upload>
        <rate></rate>
        <el-form></el-form>
        <el-table></el-table>
        <el-tag></el-tag>
        <el-progress></el-progress>
        <tree></tree>
        <pagination></pagination>
        <badge></badge>
        <alert></alert>
        <loading></loading>
        <message></message>
        <message-box></message-box>
        <notification></notification>
        <nav-menu></nav-menu>
        <tabs></tabs>
        <breadcrumb></breadcrumb>
        <dropdown></dropdown>
        <steps></steps>
        <el-dialog></el-dialog>
        <tooltip></tooltip>
        <popover></popover>
        <carousel></carousel>
        <collapse></collapse>
    </div>
</template>


<script>
    import layout from './component/layout.vue';
    import icon from './component/icon.vue';
    import btn from './component/button.vue';
    import radio from './component/radio.vue';
    import checkbox from './component/checkbox.vue';
    import elInput from './component/input.vue';
    import inputNumber from './component/inputNumber.vue';
    import elSelect from './component/select.vue';
    import elSwitch from './component/switch.vue';
    import slider from './component/slider.vue';
    import timePicker from './component/timePicker.vue';
    import datePicker from './component/datepicker.vue';
    import dateTimePicker from './component/dateTimePicker.vue';
    import upload from './component/upload.vue';
    import rate from './component/rate.vue';
    import elForm from './component/form.vue';
    import elTable from './component/table.vue';
    import elTag from './component/tag.vue';
    import elProgress from './component/progress.vue';
    import tree from './component/tree.vue';
    import pagination from './component/pagination.vue';
    import badge from './component/badge.vue';
    import alert from './component/alert.vue';
    import loading from './component/loading.vue';
    import message from './component/message.vue';
    import messageBox from './component/messageBox.vue';
    import notification from './component/notification.vue';
    import navMenu from './component/navMenu.vue';
    import tabs from './component/tabs.vue';
    import breadcrumb from './component/breadcrumb.vue';
    import dropdown from './component/dropdown.vue';
    import steps from './component/steps.vue';
    import elDialog from './component/dialog.vue';
    import tooltip from './component/tooltip.vue';
    import popover from './component/popover.vue';
    import carousel from './component/carousel.vue';
    import collapse from './component/collapse.vue';
    export default {
        data () {
            return {
                msg: 'Use Vue 2.0 Today!'
            }
        },
        components: {
            layout,icon,btn,radio,checkbox,elInput,inputNumber,elSelect,elSwitch,slider,timePicker,datePicker,dateTimePicker,upload,rate,
            elForm,elTable,elTag,elProgress,tree,pagination,badge,alert,loading,message,messageBox,notification,navMenu,tabs,breadcrumb,
            dropdown,steps,elDialog,tooltip,popover,carousel,collapse
        },
        methods: {
            startHacking () {
                this.$notify({
                    title: 'It Works',
                    message: 'We have laid the groundwork for you. Now it\'s your time to build something epic!',
                    duration: 6000
                })
            }
        }
    }
</script>

<style scoped>
    body {
        font-family: Helvetica, sans-serif;
    }
</style>
