<template>
  <div class="emphasispeople">
    <div class="search-start">
      <div class="item-title">
        数据更新时间: 2018-4-18 16:45:08
      </div>
      <el-form ref="form"
               :model="form"
               label-width="68px">
        <el-form-item label="领证机构">
          <el-select v-model="form.region"
                     placeholder="请选择">
            <el-option label="全省"
                       value="全省"></el-option>
            <el-option label="全市"
                       value="全市"></el-option>
          </el-select>
        </el-form-item>
      </el-form>
    </div>
    <!-- <el-table :data="tableData"
              style="width: 100%">
      <el-table-column prop="people-type"
                       label="人员类型">
      </el-table-column>
      <el-table-column prop="peopleNumber"
                       label="总人数">
      </el-table-column>
      <el-table-column prop="address"
                       label="有驾驶证">
      </el-table-column>
      <el-table-column prop="address"
                       label="有机动车">
      </el-table-column>
      <el-table-column prop="address"
                       label="有车有证">
      </el-table-column>
    </el-table> -->
    <info-card class="info-card"
               :height="height">
      <info-card-item v-for="(item, index) of items"
                      :key="index">
        <div class="item-wrap">
          <span class="item-type">{{item.accidentType}}</span>
          <p class="item"><span class="item-title">姓名：</span>{{item.name}}</p>
          <p class="item"><span class="item-title">身份证：</span>{{item.idcard}}</p>
          <p class="item"><span class="item-title">住址：</span>{{item.accidentResult}}</p>
          <p class="item"><span class="item-title">驾驶证状态：</span>{{item.time}}</p>
          <p class="item"><span class="item-title">车牌种类：</span>{{item.site}}</p>
          <p class="item"><span class="item-title">有无机动车：</span>{{item.car}}</p>

        </div>
      </info-card-item>
    </info-card>
  </div>
</template>

<script>
import InfoCardItem from '@/components/InfoCard/InfoCardItem'
import InfoCard from '@/components/InfoCard/InfoCard'
export default {
  data () {
    return {
      height: 'calc(100% - 30px - 35px - 20px - 20px)',
      form: {
        region: ''
      },
      items: [
        {
          name: '张威',
          accidentType: '吸毒人员',
          idcard: '429000',
          accidentResult: '武汉市',
          time: '正常',
          site: '小型汽车',
          car: '苏BC1345'
        },
        {
          name: '张威',
          accidentType: '吸毒人员',
          idcard: '429000',
          accidentResult: '武汉市',
          time: '正常',
          site: '小型汽车',
          car: '苏BC1345'
        },
        {
          name: '张威',
          accidentType: '吸毒人员',
          idcard: '429000',
          accidentResult: '武汉市',
          time: '正常',
          site: '小型汽车',
          car: '苏BC1345'
        },
        {
          name: '张威',
          accidentType: '吸毒人员',
          idcard: '429000',
          accidentResult: '武汉市',
          time: '正常',
          site: '小型汽车',
          car: '苏BC1345'
        },
        {
          name: '张威',
          accidentType: '吸毒人员',
          idcard: '429000',
          accidentResult: '武汉市',
          time: '正常',
          site: '小型汽车',
          car: '苏BC1345'
        }
      ]
    }
  },
  components: {
    InfoCardItem,
    InfoCard
  }

}
</script>

<style lang="stylus" scoped>
.search-start >>> .el-input__inner
  height 30px
.item-title
  text-align center
  color #fff
.el-form
  padding 5px 0px
</style>
