<template>
    <div>
        <div class="container text-left">
                <div class="row">
                    <div class="card" style="max-width: 50rem;">
                        <div class="card-header"><h1>Password Reset</h1></div>
                        <div class="card-body">
                            <form method="post" action="#" enctype="multipart/form-data" >
                                <div class="form-row">
                                    <div class="form-group col-sm-12  col-md-12 col-lg-12">
                                        <label ><b>New password:</b></label>
                                            <input type="password" class="form-control"  placeholder="New password" v-model="formelement.confirmedpassword">
                                    </div>
                                    <div class="form-group col-sm-12 col-md-12 col-lg-12">
                                        <label ><b>Confirm Password:</b></label>
                                            <input type="password" class="form-control"  placeholder="Re-enter password" v-model="formelement.confirmedpassword">
                                    </div>
                                    <div class="form-group col-sm-2  col-md-2  col-lg-2 "> 
                                        <button type="button" class="form-control btn btn-success" v-on:click="submitpost()" >Submit</button>
                                    </div>
                                    <div class="form-group col-sm-2  col-md-2  col-lg-2 "> 
                                        <button type="button" class="form-control btn btn-info" v-on:click="cancelpost()" >Cancel</button>
                                    </div>
                                </div>
                            </form>
                        </div>
                    </div>
                </div>
        </div>
    </div>
</template>
<script>
export default {
  data(){
      return{
          formelement:{
              newpassword:'',
              confirmedpassword:''
          }
      }
  },
  methods:{
      submitpost(){
          console.log("success");
          this.$swal({
              title: 'Congratulations',
               type: 'success',
                confirmButtonColor: "#5042f4",
                confirmButtonText: "Yes, got it!",
               text:'Your password has changed successfully'
               });
           
      },
      cancelpost(){
          console.log("cancelled");
          this.$swal({
            title: 'Sorry',
            type: 'error',
            confirmButtonColor: "red",
            confirmButtonText: "Yes, got it!",
            text:'you cancelled the process'
        });
      }
  }
 
}
</script>
<style>
.container{
    background-color: white;
    margin-top: 220px;
    margin-left:650px;
}
h1{
    text-align: center;

}


</style>

