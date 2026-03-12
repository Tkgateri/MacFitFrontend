<script setup>
import { ref } from 'vue'
import {useRouter} from "vue-router";

const router = useRouter();

const showBundleDialog = ref(false)
const isLoggedIn = localStorage.getItem("isLoggedIn")
const selectedBundle = ref(null)
const selectedPrice = ref(null)

function showBundle(name, price){
    if(isLoggedIn){
        selectedBundle.value = name
        selectedPrice.value = price
        showBundleDialog.value = true //open popup
    }else{
        router.push('/login')
    }
}
function subscribe(){
    const userDetails = JSON.parse(localStorage.getItem('userDetails'))
    userDetails.subcription ={
        name:selectedBundle.value,
        price:selectedPrice.value
    }
    localStorage.setItem('userDetails', JSON.stringify(userDetails))
    showBundleDialog.value = false
}
</script>

<template>
    <v-container style="background-color:#CFD0D6" class="mt-12">
        <v-row>
            <div class="text-display-medium mb-12">Bundles and Pricing</div>
        </v-row>
        <v-row>
            <div class="text-label-medium font-italic">Please choose your most preferred bundle</div>
        </v-row>
        <v-row>
            <v-col md="3">
                <v-card class="text-center" @click="showBundle('Daily Pass',500)">
                    <v-icon color="#7B3F8F" icon="mdi-clock-outline" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#7B3F8F">Daily Pass</v-card-title>
                    <v-card-text>Kshs. 500</v-card-text>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center" @click="showBundle('1 Month', 15000)">
                    <v-icon color="#7B3F8F" icon="mdi-calendar-account-outline" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#7B3F8F">1 month</v-card-title>
                    <v-card-text>Kshs. 15,000</v-card-text>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center" @click="showBundle('3 Months',45000)">
                    <v-icon color="#7B3F8F" icon="mdi-numeric-3-circle" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#7B3F8F">3 Months</v-card-title>
                    <v-card-text>Kshs. 45,000</v-card-text>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center" @click="showBundle('6 Months',54000)">
                    <v-icon color="#7B3F8F" icon="mdi-numeric-6-box-multiple-outline" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#7B3F8F">6 Months</v-card-title>
                    <v-card-text>Kshs. 54,000</v-card-text>
                </v-card>
            </v-col>
        </v-row>
              <v-row>
            <v-col md="12">
                <v-card class="text-center" @click="showBundle('12 Months',70000)">
                    <v-icon color="#7B3F8F" icon="mdi-timer-sand-full" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#3A4B68">12 Months</v-card-title>
                    <v-card-text>Kshs. 70,000</v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
    <!-- What is included? -->
     <v-container style="background-color:#CFD0D6" class="mt-12">
        <v-row>
            <div class="text-display-medium mb-12">What is included?</div>
        </v-row>
        <v-row>
            <v-col md="3">
                <v-card class="text-center">
                    <v-icon color="#7B3F8F" icon="mdi-food-apple-outline" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#7B3F8F">Personalized Diet Plans</v-card-title>
                   
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center">
                    <v-icon color="#7B3F8F" icon="mdi-weight-lifter" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#7B3F8F">Gym Membership Card</v-card-title>
                    
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center">
                    <v-icon color="#7B3F8F" icon="mdi-hours-24" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#7B3F8F">24/7 Cosultation</v-card-title>
                    
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center">
                    <v-icon color="#7B3F8F" icon="mdi-swim" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#7B3F8F">Access to a pool</v-card-title>
                </v-card>
            </v-col>           
        </v-row>
        </v-container>
        <v-container style="background-color:#CFD0D6" class="mt-12">
            <v-row>
            <div class="text-display-medium mb-12">How to Join</div>
            </v-row>
        <v-row>
            <v-col>
                <v-list>
                    <v-list-item>1. Register for membership through our website. </v-list-item>
                    <v-list-item>2. Select a bundle that best suites you and make payment through Mpesa payblill number 555000.</v-list-item>
                    <v-list-item>3. Forward the payment confirmation message to our email address "macfitgym@gmail.com"</v-list-item>
                    <v-list-item>4. Finally, make an appearance at our gym and begin your transformation journey! </v-list-item>
                </v-list>
            </v-col>
        </v-row>
     </v-container>
     <!-- Dialog -->
        <v-dialog v-model="showBundleDialog" max-width="600" >

      <v-card prepend-icon="mdi-account" title="Subscribe to Bundle" >
        <v-card-text>
          You are about to subscribe to {{ selectedBundle }} at {{ selectedPrice }}. Click on the button below to complete payment
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
         <v-spacer></v-spacer>
          <v-btn text="Close" variant="plain" @click="showBundleDialog = false" ></v-btn>
          <v-btn color="primary" variant="tonal" @click="subscribe()" >Subscribe</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
</template>