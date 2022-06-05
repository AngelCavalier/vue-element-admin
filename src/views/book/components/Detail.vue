<template>
  <el-form ref="postForm" :model="postForm">
    <sticky :class-name="'sub-navbar'">
      <el-button v-if="!isEdit" @click="showGuide">显示帮助</el-button>
      <el-button v-loading="loading" type="success" style="margin-left: 10px" @click="submitForm">
        {{ isEdit ? '编辑电子书':'新增电子书' }}
      </el-button>
    </sticky>
    <div class="detail-container">
      <el-row>
        <waring />
        <el-col :span="24">
          <EbookUpload />
        </el-col>
        <el-col :span="24">11</el-col>
      </el-row>
    </div>
  </el-form>
</template>

<script>
import Sticky from '@/components/Sticky'
import Waring from './Warning'
import EbookUpload from '@/components/EbookUpload'

export default {
  components: { Sticky, Waring, EbookUpload },
  props: {
    isEdit: Boolean
  },
  data() {
    return {
      loading: false,
      postForm: {

      }
    }
  }
}
</script>

<style lang="scss" scoped>
  .detail-container {
    padding: 40px 50px 20px;

    .preview-img {
      width: 200px;
      height: 270px;
    }
  }
</style>
