  <template>
<div>
    <el-table :data="tableData" style="width: 100%">
    <el-table-column prop="id" label="ID" width="180"> </el-table-column>
    <el-table-column prop="name" label="Name" width="280"> </el-table-column>
    <el-table-column prop="boss" label="Boss" width="180"> </el-table-column>
    <el-table-column prop="member" label="Member" width="300"></el-table-column>
    <el-table-column
      prop="address"
      label="Address"
      width="280"
    ></el-table-column>
    <el-table-column prop="date" label="Date" > </el-table-column>
  </el-table>
  <Form />
</div>
</template>

  <script>
    import Form from './Form.vue'
export default {
    components:{
    Form
  },
  data() {
    return {
      tableData: [
        {
          id: "1",
          name: "AI Camera",
          boss: "Tung Ho",
          member: "Dao NC, Hao HT",
          address: "No. 189, Grove St, Los Angeles",
          date: "2021-05-03",
        },
        {
          id: "2",
          name: "Smart Banking API",
          boss: "Tung Ho",
          member: "Hao HT, Binh PT, Son TH ",
          address: "No. 189, Grove St, Los Angeles",
          date: "2021-08-03",
        },
        {
          id: "3",
          name: "Construct Management",
          boss: "Tung Ho",
          member: "Dao NC, Trung VV, Manh BĐ",
          address: "No. 189, Grove St, Los Angeles",
          date: "2021-08-01",
        },
        {
          id: "4",
          name: "Fuel Management",
          boss: "Tung Ho",
          member: "Dao NC, Hao HT, Thuan HQ, Thong NV",
          address: "No. 189, Grove St, Los Angeles",
          date: "2021-08-05",
        },
      ],
    };
  },
};
</script>