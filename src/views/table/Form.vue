<template>
<div>
  <el-button type="text" @click="dialogFormVisible = true">Add Project</el-button>

<el-dialog title="Add Project" :visible.sync="dialogFormVisible" @confirm = "handleConfirm">
  <el-form :model="form" @submit.stop.prevent="handleSubmit">
        <el-form-item label="ID" :label-width="formLabelWidth" >
      <el-input v-model="form.id" autocomplete="off"></el-input>
    </el-form-item>
    <el-form-item label="Name" :label-width="formLabelWidth">
      <el-input v-model="form.name" autocomplete="off"></el-input>
    </el-form-item>
        <el-form-item label="Boss" :label-width="formLabelWidth">
      <el-input v-model="form.boss" autocomplete="off"></el-input>
    </el-form-item>
        <el-form-item label="Member" :label-width="formLabelWidth">
      <el-input v-model="form.member" autocomplete="off"></el-input>
    </el-form-item>
        <el-form-item label="Address" :label-width="formLabelWidth">
      <el-input v-model="form.address" autocomplete="off"></el-input>
    </el-form-item>
        <el-form-item label="Date" :label-width="formLabelWidth">
      <el-input v-model="form.date" autocomplete="off"></el-input>
    </el-form-item>
  </el-form>
  <span slot="footer" class="dialog-footer">
    <el-button @click="dialogFormVisible = false">Cancel</el-button>
    <el-button type="primary" @click="dialogFormVisible = false">Confirm</el-button>
  </span>
</el-dialog>
</div>
</template>

<script>
  export default {
    data() {
      return {
        project:{
          id: Math.floor(Math.random()),
          name: "",
          boss: "",
          member: "",
          address: "",
          date: "",
        },
        dialogFormVisible: false,
        form: {
          name: '',
          region: '',
          date1: '',
          date2: '',
          delivery: false,
          type: [],
          resource: '',
          desc: ''
        },
        formLabelWidth: '120px'
      };
    },
    methods: {
      handleConfirm(bvModalEvt) {
        this.$emit("save",this.member)
        // Prevent modal from closing
        bvModalEvt.preventDefault()
        // Trigger submit handler
        this.handleSubmit()
      },
      handleSubmit() {
        // Exit when the form isn't valid
        if (!this.checkFormValidity()) {
          return
        }
        // Push the name to submitted names
        this.submittedNames.push(this.name)
        // Hide the modal manually
        this.$nextTick(() => {
          this.$bvModal.hide('modal-prevent-closing')
        })
      }
    }
  };
</script>