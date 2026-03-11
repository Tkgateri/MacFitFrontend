<script setup>
import { ref } from 'vue'

  const rules = {
    required: value => !!value || 'Required.',
    min: v => v.length >= 8 || 'Min 8 characters',
    passwordMatch: () => password === confirmPassword || `Password must match`,
  }

  const show1 = ref(false)
  const show2 = ref(true)
  const password = ref(null) 
  

  
  const confirmPassword = ref(null)
  const show1confirm = ref(false)

  //models
  const firstName = ref(null)
  const lastName = ref(null)
  const email = ref(null)
  const phoneNumber = ref(null)
  const gender = ref(null)
  const dob = ref(null)
  const gymLocation = ref(null)

  function signUp(){
    //create user object (pretty much holds client details)

    const userDetails = {
        name : firstName.value + lastName.value,
        email:email.value,
        phone:phoneNumber.value,
        dob:dob.value,
        gender:gender.value,
        gymLocation:gymLocation.value,
        password:password.value,

    }

    //store data
    try{
        localStorage.setItem('userDetails', JSON.stringify(userDetails))
    }catch(err){
        console.error('Sign up process faied',err)

    }
  }

</script>
<template>
    <v-container width="50%" class="text-center mt-12" color="#CFD0D6">
        <v-row>
            <v-col>
                <v-form>
                    <v-row>
                        <v-col md="12">
                            <v-image src="/logo.png" width="40%" height="40%"></v-image>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col>
                            <div class="text-display-small font-weight-medium">Sign in to MacFit Gym</div>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">First Name</div>
                        </v-col>
                        <v-col md="6">
                            <v-text-field variant="outlined" v-model="firstName"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Last Name</div>
                        </v-col>
                        <v-col md="6">
                            <v-text-field variant="outlined" v-model="lastName"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Email</div>
                        </v-col>
                        <v-col md="6">
                            <v-text-field variant="outlined" v-model="email"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Phone</div>
                        </v-col>
                        <v-col md="6">
                            <v-text-field variant="outlined" type="number" v-model="phonenumber"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Gender</div>
                        </v-col>
                        <v-col md="6">
                            <v-radio-group inline v-model="gender">
                                <v-radio label="Male" value="Male"></v-radio>
                                <v-radio label="Female" value="Female"></v-radio>
                            </v-radio-group>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Date of Birth</div>
                        </v-col>
                        <v-col md="6">
                            <v-date-input variant="outline" v-model="dob"></v-date-input>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Gym Location</div>
                        </v-col>
                        <v-col md="6">
                            <v-select
                                label="Select"
                                :items="['CBD', 'Madaraka', 'Westlands', 'Buruburu',]"
                                v-model="gymLocation">

                                </v-select>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Password</div>
                        </v-col>
                        <v-col md="6">
                            <v-text-field
                            variant="outlined"
                            v-model="password"
                            :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                            :rules="[rules.required, rules.min]"
                            :type="show1 ? 'text' : 'password'"
                            name="input-10-1"
                            @click:append="show1 = !show1"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Confirm Password</div>
                        </v-col>
                        <v-col md="6">
                            <v-text-field
                            variant="outlined"
                            v-model="confirmPassword"
                            :append-icon="show1confirm ? 'mdi-eye' : 'mdi-eye-off'"
                            :rules="[rules.required, rules.min, rules.passwordMatch,]"
                            :type="show1 ? 'text' : 'password'"
                            name="input-10-1"
                            @click:append="show1 = !show1"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="12">
                            <v-btn color="#CFD0D6" variant="elevated" @click="signUp" width="25%">Sign Up</v-btn>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="12">
                            <div>Already have an account?
                                <router-link to="/login">Login</router-link>
                            </div>
                        </v-col>
                    </v-row>
                </v-form>
            </v-col>
        </v-row>
    </v-container>
</template>