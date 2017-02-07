<template>
    <div class="tag">
        <el-tag
                v-for="(tag,index) in tags"
                :closable="true"
                :close-transition="false"
                :type="tag.type"
                @close="handleDelete(index)"
        >
            {{tag.name}}
        </el-tag>

        <el-input
                class="input-new-tag"
                v-if="inputVisible"
                v-model="inputValue"
                ref="saveTagInput"
                size="mini"
                @keyup.enter.native="handleInputConfirm"
                @blur="handleInputConfirm"
        >
        </el-input>
        <el-button v-else class="button-new-tag" size="small" @click="showInput">+ New Tag</el-button>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                tags: [
                    { name: '标签一', type: '' },
                    { name: '标签二', type: 'gray' },
                    { name: '标签三', type: 'primary' },
                    { name: '标签四', type: 'success' },
                    { name: '标签五', type: 'warning' },
                    { name: '标签六', type: 'danger' }
                ],
                inputVisible: false,
                inputValue: ''
            };
        },
        methods: {
            handleDelete(index) {
                this.tags.splice(index, 1);
            },

            showInput() {
                this.inputVisible = true;
            },

            handleInputConfirm() {
                let inputValue = this.inputValue;
                if (inputValue) {
                    this.tags.push({name:inputValue, type: ''});

                }
                console.log(this.tags);
                this.inputVisible = false;
                this.inputValue = '';
            }
        }
    }
</script>
<style scoped>
    .tag{
        margin-top:10px;
    }
</style>