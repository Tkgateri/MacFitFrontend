<script setup>

</script>

<template>
    <v-container max width ="100%">
        <v-row>
            <v-carousel>
                <v-carousel-item src="landscape1.jpg"></v-carousel-item>
                <v-carousel-item src="landscape2.jpg"></v-carousel-item>
                <v-carousel-item src=""></v-carousel-item>
            </v-carousel>
        </v-row>
    </v-container>

    <!-- About Us -->
     <v-container style="background-color:#CFD0D6" max width =100%>
        <v-row >
            <v-col md="8" class="text-center">
                <div class="text-display-medium mb-12">Welcome to MacFit Gym</div>
                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Welcome to MacFit, a place where sweat turns into strength and goals stop being “someday” ideas. MacFit was built for people who want more from their fitness journey, whether that means lifting heavier, running faster, or simply feeling better every day. Our gym blends modern equipment, expert guidance, and an energetic atmosphere to create a space where every workout moves you closer to the strongest version of yourself. Think of it as your personal launchpad for health and performance.</div>
                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">At MacFit, fitness is not a one-size-fits-all routine. Our facility offers a wide range of training options, from strength and conditioning zones to cardio stations and functional workout areas designed to challenge every muscle. Members can access professional trainers, structured programs, and supportive coaching that help transform effort into real, visible progress. Whether you are a beginner stepping into the gym for the first time or an experienced athlete refining your craft, MacFit is designed to meet you where you are and push you further.</div>
                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">More than just a gym, MacFit is a community. Here, motivation is contagious, progress is celebrated, and every member becomes part of a culture built on discipline, resilience, and growth. From the first rep to the final stretch of your workout, you are surrounded by people who share the same drive to improve. Join MacFit and experience a fitness environment where commitment meets community and every day is another step toward a healthier, stronger life.</div>
                <v-btn>LEARN MORE</v-btn>
            </v-col>
            <v-col md="4">
            <v-container md="6" class="d-flex align-center justify-center fill-height">
                <v-img src="aboutus.jpg" cover></v-img>
            </v-container>
            </v-col>
        </v-row>
     </v-container>
     <!-- LATEST NEWS -->
<v-container>
        <v-row>
            <v-col md="4">
                <v-card>
                    <v-img src="aerobics.jpg" cover></v-img>
                    <v-card-title>Did You Know?</v-card-title>
                    <v-card-text>Aerobic exercise, also known as "cardio," is a rhythmic and repetitive activity that engages large muscle groups to strengthen the heart and lungs. By increasing heart and respiratory rates, aerobics enhances the body's ability to efficiently transport and use oxygen.</v-card-text>
                    <v-btn color="#3A4B68">READ MORE</v-btn>
                </v-card>
            </v-col>
            <v-col md="4">
                <v-card>
                    <v-img src="treadmill.jpg" cover></v-img>
                    <v-card-title>Did You Know?</v-card-title>
                    <v-card-text>Running on a treadmill offers a highly efficient way to improve cardiovascular health and maintain a healthy weight through controlled calorie-burning workouts. Unlike outdoor surfaces, treadmill decks often feature shock-absorbing technology that reduces impact on the knees and joints, making it a safer option for those prone to injury. These machines provide total control over training variables like speed and incline, allowing users to precisely customize their intensity and track progress in real time.</v-card-text>
                    <v-btn color="#3A4B68">READ MORE</v-btn>
                </v-card>
            </v-col>
            <v-col md="4">
                <v-card>
                    <v-img src="healthyeating.jpg" cover></v-img>
                    <v-card-title>Did You Know?</v-card-title>
                    <v-card-text>Combining a nutrient-dense diet with a consistent exercise routine creates a powerful synergy that far exceeds the results of either practice alone. While a balanced diet provides the essential "fuel" and building blocks for muscle repair and energy, regular physical activity accelerates metabolic efficiency and preserves lean muscle mass during weight loss. This dual approach is highly effective in managing body weight and significantly reducing the risk of chronic conditions like type 2 diabetes, hypertension, and cardiovascular disease. </v-card-text>
                    <v-btn color="#3A4B68">READ MORE</v-btn>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

<!-- REVIEWS -->
<v-container>
    <v-row>
        <v-col md="3">
            <v-card>
                <v-card-text>10 out of 10</v-card-text>
                <v-rating :length="5" :size="32" :model-value="3" active-color="primary"></v-rating>
            </v-card>
        </v-col>
        <v-col md="3">
            <v-card>
                <v-card-text>Absolutely loved the trainers and everything about the gym. Highly Recommend</v-card-text>
                <v-rating :length="5" :size="32" :model-value="3" active-color="primary"></v-rating>
            </v-card>
        </v-col>
        <v-col md="3">
            <v-card>
                <v-card-text>Up to date equipment with highly trained professionals. Awesome</v-card-text>
                <v-rating :length="5" :size="32" :model-value="3" active-color="primary"></v-rating>
            </v-card>
        </v-col>
    </v-row>
</v-container>

<!-- CONTACT US -->
<v-container>
    <v-row class="text-center">
        <div class="text-title-large font-weight-light text-medium-emphasis mb-8"> Contact Us</div>
        <div class="text-title-large font-weight-light text-medium-emphasis mb-8">0755550000 | macfitgym@gmail.com</div>
        <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Opening Hours</div>
        <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Monday-Friday: 5.00am - 9.00pm | Saturday-Sunday: 6.00am-6.00pm</div>
        <div class="text-title-large font-weight-light text-medium-emphasis mb-8"></div>
        <div class="text-title-large font-weight-light text-medium-emphasis mb-8"></div>
        
       
    </v-row>
</v-container>
</template>