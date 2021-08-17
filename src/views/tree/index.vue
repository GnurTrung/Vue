  <template>
<div>
  <title>ahihi</title>
  <el-table :data="tableData" style="width: 100%">
    <el-table-column prop="id" label="ID" width="180"> </el-table-column>
    <el-table-column prop="name" label="Name" width="180"> </el-table-column>
    <el-table-column prop="phone" label="Phone" width="180"> </el-table-column>
    <el-table-column prop="credit" label="Credit Card" width="180"></el-table-column>
    <el-table-column
      prop="address"
      label="Address"
      width="280"
    ></el-table-column>
    <el-table-column prop="date" label="Date" > </el-table-column>
  </el-table>
      <Add @save ="clickAdd" />
</div>
</template>

  <script>
  import Add from './Add.vue'
export default {
  components:{
    Add
  },
  data() {
    return {
      tableData: [
        {
          id: "1",
          name: "Vu Trung",
          phone: "0123456789",
          credit: "1900123456",
          address: "No. 189, Grove St, Los Angeles",
          date: "2021-05-03",
        },
        {
          id: "2",
          name: "Bui Manh",
          phone: "0123456789",
          credit: "1900123456",
          address: "No. 189, Grove St, Los Angeles",
          date: "2021-08-03",
        },
        {
          id: "3",
          name: "Hoang Thuan",
          phone: "0123456789",
          credit: "1900123456",
          address: "No. 189, Grove St, Los Angeles",
          date: "2021-08-01",
        },
        {
          id: "4",
          name: "Pham Binh",
          phone: "0123456789",
          credit: "1900123456",
          address: "No. 189, Grove St, Los Angeles",
          date: "2021-08-05",
        },
      ],
    };
  },
  methods:{
    clickAdd(itemSave){
      this.items.push(itemSave)
    }
  }
};
</script>