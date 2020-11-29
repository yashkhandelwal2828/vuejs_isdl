<template>
  <form>
    <b-card>
      <b-card-header
        header-text-variant="light"
        header-border-variant="none"
        style="
          background: linear-gradient(60deg, #66bb6a, #43a047);
          margin: -30px 0px 0px;
           box-shadow: 0 10px 30px -12px rgba(0,0,0,.42)
        "
      >
        <h4 class="title">Edit Profile</h4>
        <p class="category">Complete your profile</p>
      </b-card-header>

      <b-card-content>
        <b-form>
    
          <div class="w-100 input">
            <!-- <div class="w-33"> -->
              <!-- <b-form-group
                label="Company(Disabled)"
                label-for="input-1"
                
              > -->
              <!-- <div class="w-33"> -->
                <b-form-input class="mb-4 mt-4 mr-sm-2 ml-sm-2 mb-sm-0"  id="input-1" placeholder="Company(Disabled)" disabled></b-form-input>
              <!-- </div> -->
              <!-- </b-form-group> -->
            <!-- </div> -->

   

            <!-- <div class="w-33"> -->
              <!-- <b-form-group
                label="User Name"
                label-for="input-2"
        
              > -->
              <!-- <div class="w-33"> -->
                <b-form-input class="mb-4 mt-4 mr-sm-2 ml-sm-2 mb-sm-0"  placeholder="User Name" id="input-2"></b-form-input>
                <!-- </div> -->
              <!-- </b-form-group> -->
            <!-- </div> -->
       
            <!-- <b-form-group
              label="Email Address"
              label-for="input-3"
              class="w-35"
            > -->
            <!-- <div class="w-33"> -->
              <b-form-input class="mb-4 mt-4 mr-sm-2 ml-sm-2 mb-sm-0" placeholder="Email Address"  id="input-3"></b-form-input>
            <!-- </div> -->
            <!-- </b-form-group> -->
          </div>
          <div class="w-100 input">
                <b-form-input class="mb-4 mt-4 mr-sm-2 ml-sm-2 mb-sm-0"  placeholder="First Name" id="input-2"></b-form-input>
                <b-form-input class="mb-4 mt-4 mr-sm-2 ml-sm-2 mb-sm-0"  placeholder="Last Name" id="input-2"></b-form-input>

          </div>
 
          <div class="w-100" style="margin-top: 21px">
            <b-form-input
              :id="type - text"
              class="mr-sm-2 ml-sm-2 mb-4 mt-4"
              placeholder="Address"
            ></b-form-input>
          </div>
          <div class="w-100 input">
          <!--<div class="w-33" style="margin-top: 21px; margin:auto;">-->
            <b-form-input class="mb-4 mt-4 mr-sm-2 ml-sm-2 mb-sm-0" :id="type - text" placeholder="City"></b-form-input>
          <!--</div>-->
   
          <!--<div class="w-33" style="margin-top: 21px; margin:auto;">-->
            <b-form-input class="mb-4 mt-4 mr-sm-2 ml-sm-2 mb-sm-0"
              :id="type - text"
              placeholder="Country"
            ></b-form-input>
          <!--</div>-->
        
          <!--<div class="w-33" style="margin-top: 21px; margin:auto;">-->
            <b-form-input class="mb-4 mt-4 mr-sm-2 ml-sm-2 mb-sm-0"
              :id="type - number"
              :number="number"
              placeholder="Postal Code"
            ></b-form-input>
          </div>

          <div class="w-100">
            <b-form-group class="mt-4 label" label="About Me">
              <b-form-textarea
                id="textarea"
                v-model="aboutme"
                class="mb-4"
                placeholder="About Me"
                rows="4"
              ></b-form-textarea>
            </b-form-group>
          </div>

          <!--<div class="md-layout-item md-size-100 text-right">
            <md-button class="md-raised md-success">Update Profile</md-button>
          </div>-->
          <div class="text-right">
          <b-button v-if="isHovered" size="sm"  href="#" variant="success" style="background-color:#4caf50 !important; color:white !important; padding:12px 25px;">
            <p>UPDATE PROFILE</p>
        </b-button>
        <b-button v-else size="sm"  href="#" variant="success" style="background-color:#4caf50 !important; color:white !important; padding:12px 25px; ">
            <p>UPDATE PROFILE</p>
        </b-button>
        </div>
        </b-form>
      </b-card-content>
    </b-card>
  </form>
</template>

<script>
export default {
    name: "edit-profile-form",
    props: {
        dataBackgroundColor: {
            type: String,
            default: ""
        }
    },
    data() {
        return {
            username: null,
            disabled: null,
            emailadress: null,
            lastname: null,
            firstname: null,
            address: null,
            city: null,
            country: null,
            code: null,
            aboutme: "Lamborghini Mercy, Your chick she so thirsty, I'm in that two seat Lambo."
        };
    }
};
</script>

<style>
  .input{
    display: flex;
    justify-content: space-around;
  }
 legend{
   padding: 0 !important;
 }
</style>
