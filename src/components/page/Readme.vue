<template lang="html">
	<div class="">
		<el-carousel :interval="4000" type="card" height="200px" class="my-carousel">
	    <el-carousel-item v-for="item in imgList" :key="item">
	      <img :src="item" />
	    </el-carousel-item>
	  </el-carousel>

		<el-table :data="tableData" class="my-table" style="width: 100%">
	    <el-table-column prop="date" label="日期" width="180">
	    </el-table-column>
	    <el-table-column prop="name" label="姓名" width="180">
	    </el-table-column>
	    <el-table-column prop="address" label="地址">
	    </el-table-column>
	  </el-table>
	</div>

</template>

<script>
export default {
	data() {
		return {
			imgList: [
				'../../static/images/a.jpeg',
				'../../static/images/b.jpeg',
				'../../static/images/c.jpeg',
				'../../static/images/d.jpeg',
				'../../static/images/e.jpeg'
			],
			tableData: [{
        date: '2017-09-30',
        name: 'why',
        address: '上海市徐汇区漕河泾开发区'
      }, {
        date: '2017-09-30',
        name: 'why',
        address: '上海市徐汇区漕河泾开发区'
      }, {
        date: '2017-09-30',
        name: 'why',
        address: '上海市徐汇区漕河泾开发区'
      }, {
        date: '2017-09-30',
        name: 'why',
        address: '上海市徐汇区漕河泾开发区'
      }]

		}
	}
}
</script>

<style lang="css" scoped>
.el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 200px;
    margin: 0;
  }

  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
	.my-carousel{max-width: 800px;min-width: 900px;width: auto;}
	.my-table{margin-top: 100px;}
</style>
