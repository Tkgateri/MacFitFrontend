<script setup>
import { ref } from 'vue'

  const rules = {
    required: value => !!value || 'Required.',
    min: v => v.length >= 8 || 'Min 8 characters',
    emailMatch: () => (`The email and password you entered don't match`),
  }

  const show1 = ref(false)
  const show2 = ref(true)
  const password = ref(null)
  const confirmPassword = ref(null)
  const show1confirm = ref(false)

</script>
<template>
    <v-container width="50%" class="text-center mt-12" color="#CFD0D6">
        <v-row>
            <v-col>
                <v-form>
                    <v-row>
                        <v-col md="12">
                            <v-icon size="large">mdi-dumbbell</v-icon>
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
                            <v-text-field variant="outlined"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Last Name</div>
                        </v-col>
                        <v-col md="6">
                            <v-text-field variant="outlined"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Email</div>
                        </v-col>
                        <v-col md="6">
                            <v-text-field variant="outlined"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Phone</div>
                        </v-col>
                        <v-col md="6">
                            <v-text-field variant="outlined" type="number"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Gender</div>
                        </v-col>
                        <v-col md="6">
                            <v-radio-group inline>
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
                            <v-date-input variant="outline"></v-date-input>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="6">
                            <div class="text-display-small font-weight-medium text-right">Gym Location</div>
                        </v-col>
                        <v-col md="6">
                            <v-select
                                label="Select"
                                :items="['CBD', 'Madaraka', 'Westlands', 'Buruburu',]">

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
                            :rules="[rules.required, rules.min]"
                            :type="show1 ? 'text' : 'password'"
                            name="input-10-1"
                            @click:append="show1 = !show1"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="12">
                            <v-btn color="#CFD0D6" variant="elevated" width="25%">Log in</v-btn>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="12">
                            <div>New to MacFit Gym? Create an account</div>
                        </v-col>
                    </v-row>
                </v-form>
            </v-col>
        </v-row>
    </v-container>
</template>