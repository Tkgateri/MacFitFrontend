<script setup>

</script>

<template>
    <v-carousel height="100vh" hide-delimiters show-arrows="hover">
        <v-carousel-item>
          <v-img src="landscape1.jpg" height="100vh" cover></v-img>
        </v-carousel-item>
        <v-carousel-item>
            <v-img src="landscape2.jpg" height="100vh" cover></v-img>
        </v-carousel-item>
        <v-carousel-item >
            <v-img src="healthyeating.jpg" height="100vh" cover></v-img>
        </v-carousel-item>
    </v-carousel>
     
    <!-- About Us -->
   <!-- ===== ABOUT US ===== -->
  <v-container fluid style="background-color: #0A0A0A; padding: 80px 40px;">
    <v-row align="center" justify="center">

      <!-- Text Side -->
      <v-col cols="12" md="7" class="pr-8">
        <div style="color:#E53935; font-size:0.75rem; letter-spacing:0.3em;
                    font-weight:600; margin-bottom:12px; text-transform:uppercase;">
          Who We Are
        </div>
        <div style="color:#ffffff; font-size:2.8rem; font-weight:800;
                    text-transform:uppercase; line-height:1.1; margin-bottom:24px;">
          Welcome to <span style="color:#E53935;">MacFit Gym</span>
        </div>
        <p style="color:#cccccc; font-size:1rem; line-height:1.8;
                  font-weight:300; margin-bottom:16px;">
          Welcome to MacFit, a place where fitness meets community...
        </p>
        <p style="color:#cccccc; font-size:1rem; line-height:1.8;
                  font-weight:300; margin-bottom:16px;">
          At MacFit, fitness is not just a hobby — it's a lifestyle...
        </p>
        <p style="color:#cccccc; font-size:1rem; line-height:1.8;
                  font-weight:300; margin-bottom:32px;">
          More than just a gym, MacFit is a movement...
        </p>
        <v-btn rounded="0" style="background-color:#E53935; color:white;
               letter-spacing:0.15em; font-weight:600; padding:0 32px; height:48px;">
          LEARN MORE
        </v-btn>
      </v-col>

      <!-- Image Side -->
      <v-col cols="12" md="5">
        <v-img src="aboutus.jpg" cover height="450"
               style="border-left: 4px solid #E53935;"></v-img>
      </v-col>

    </v-row>
  </v-container>

  <!-- ===== LATEST NEWS ===== -->
  <v-container fluid style="background-color:#111111; padding:80px 40px;">
    <v-row justify="center" class="mb-10">
      <v-col cols="12" class="text-center">
        <div style="color:#E53935; font-size:0.75rem; letter-spacing:0.3em;
                    font-weight:600; margin-bottom:12px; text-transform:uppercase;">
          Stay Informed
        </div>
        <div style="color:#ffffff; font-size:2.8rem; font-weight:800;
                    text-transform:uppercase;">
          Latest <span style="color:#E53935;">News</span>
        </div>
      </v-col>
    </v-row>

    <v-row justify="center">

      <!-- Card 1 -->
      <v-col cols="12" md="4">
        <v-card style="background-color:#1a1a1a; border:1px solid #2a2a2a;
                       border-radius:0; height:100%;">
          <v-img src="aerobics.jpg" height="220" cover></v-img>
          <v-card-title style="color:#ffffff; font-size:1rem;
                               font-weight:700; padding:20px 20px 8px;
                               text-transform:uppercase; letter-spacing:0.05em;">
            Did You Know?
          </v-card-title>
          <v-card-text style="color:#aaaaaa; font-size:0.9rem;
                              line-height:1.7; padding:0 20px 20px;">
            Aerobic exercise, also known as "cardio," is a rhythmic and
            repetitive activity that strengthens your heart and lungs.
          </v-card-text>
          <v-card-actions style="padding:0 20px 20px;">
            <v-btn variant="text"
                   style="color:#E53935; letter-spacing:0.1em;
                          font-size:0.8rem; font-weight:600; padding:0;">
              READ MORE →
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>

      <!-- Card 2 -->
      <v-col cols="12" md="4">
        <v-card style="background-color:#1a1a1a; border:1px solid #2a2a2a;
                       border-radius:0; height:100%;">
          <v-img src="landscape1.jpg" height="220" cover></v-img>
          <v-card-title style="color:#ffffff; font-size:1rem;
                               font-weight:700; padding:20px 20px 8px;
                               text-transform:uppercase; letter-spacing:0.05em;">
            Up to Date Equipment
          </v-card-title>
          <v-card-text style="color:#aaaaaa; font-size:0.9rem;
                              line-height:1.7; padding:0 20px 20px;">
            Up to date equipment with highly trained professionals.
            Awesome facilities await you at MacFit.
          </v-card-text>
          <v-card-actions style="padding:0 20px 20px;">
            <v-btn variant="text"
                   style="color:#E53935; letter-spacing:0.1em;
                          font-size:0.8rem; font-weight:600; padding:0;">
              READ MORE →
            </v-btn>
          </v-card-actions>
          <v-card-text style="padding: 0 20px 20px;">
            <v-rating :length="5" :size="20" :model-value="3"
                      active-color="#E53935" color="#444"></v-rating>
          </v-card-text>
        </v-card>
      </v-col>

      <!-- Card 3 — add more as needed -->
      <v-col cols="12" md="4">
        <v-card style="background-color:#E53935; border-radius:0; height:100%;">
          <v-img src="healthyeating.jpg" height="220" cover></v-img>
          <v-card-title style="color:#ffffff; font-size:1rem;
                               font-weight:700; padding:20px 20px 8px;
                               text-transform:uppercase; letter-spacing:0.05em;">
            Healthy Eating Tips
          </v-card-title>
          <v-card-text style="color:rgba(255,255,255,0.85); font-size:0.9rem;
                              line-height:1.7; padding:0 20px 20px;">
            Fuel your workouts with the right nutrition.
            Our trainers share top tips for eating well and training hard.
          </v-card-text>
          <v-card-actions style="padding:0 20px 20px;">
            <v-btn variant="text"
                   style="color:#ffffff; letter-spacing:0.1em;
                          font-size:0.8rem; font-weight:600; padding:0;">
              READ MORE →
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>

    </v-row>
  </v-container>

<!-- REVIEWS -->
<v-container fluid style="background-color:#0A0A0A; padding:80px 40px;">

  <!-- Section Header -->
  <v-row justify="center" class="mb-10">
    <v-col cols="12" class="text-center">
      <div style="color:#E53935; font-size:0.75rem; letter-spacing:0.3em;
                  font-weight:600; margin-bottom:12px; text-transform:uppercase;">
        What Members Say
      </div>
      <div style="color:#ffffff; font-size:2.8rem; font-weight:800;
                  text-transform:uppercase;">
        Real People. <span style="color:#E53935;">Real Results.</span>
      </div>
    </v-col>
  </v-row>

  <!-- Review Cards -->
  <v-row justify="center">

    <!-- Card 1 -->
    <v-col cols="12" md="4">
      <v-card style="background-color:#1a1a1a; border:1px solid #2a2a2a;
                     border-radius:0; height:100%; padding:32px;">
        <!-- Quote mark -->
        <div style="font-size:5rem; line-height:0.8; color:#E53935;
                    opacity:0.4; font-weight:900; margin-bottom:16px;">"</div>

        <v-card-text style="color:#cccccc; font-size:0.95rem; line-height:1.8;
                            font-weight:300; padding:0; margin-bottom:24px;">
          10 out of 10. MacFit completely changed how I approach fitness.
          The energy here is unmatched!
        </v-card-text>

        <v-rating :length="5" :size="20" :model-value="5"
                  active-color="#E53935" color="#333"
                  style="margin-bottom:20px;"></v-rating>

        <!-- Author -->
        <div style="display:flex; align-items:center; gap:12px;">
          <div style="width:44px; height:44px; background:#E53935;
                      display:flex; align-items:center; justify-content:center;
                      font-size:1.2rem; font-weight:800; color:white; flex-shrink:0;">
            J
          </div>
          <div>
            <div style="color:#ffffff; font-weight:600; font-size:0.9rem;">Jordan M.</div>
            <div style="color:#666; font-size:0.8rem;">Member for 2 years</div>
          </div>
        </div>
      </v-card>
    </v-col>

    <!-- Card 2 — Featured (red) -->
    <v-col cols="12" md="4">
      <v-card style="background-color:#E53935; border-radius:0;
                     height:100%; padding:32px;">
        <div style="font-size:5rem; line-height:0.8; color:rgba(255,255,255,0.3);
                    font-weight:900; margin-bottom:16px;">"</div>

        <v-card-text style="color:#ffffff; font-size:0.95rem; line-height:1.8;
                            font-weight:300; padding:0; margin-bottom:24px;">
          Absolutely loved the trainers and everything about the gym.
          Highly recommend MacFit to anyone serious about their goals!
        </v-card-text>

        <v-rating :length="5" :size="20" :model-value="5"
                  active-color="#ffffff" color="rgba(255,255,255,0.3)"
                  style="margin-bottom:20px;"></v-rating>

        <div style="display:flex; align-items:center; gap:12px;">
          <div style="width:44px; height:44px; background:#ffffff;
                      display:flex; align-items:center; justify-content:center;
                      font-size:1.2rem; font-weight:800; color:#E53935; flex-shrink:0;">
            A
          </div>
          <div>
            <div style="color:#ffffff; font-weight:600; font-size:0.9rem;">Alicia T.</div>
            <div style="color:rgba(255,255,255,0.7); font-size:0.8rem;">Pro Member</div>
          </div>
        </div>
      </v-card>
    </v-col>

    <!-- Card 3 -->
    <v-col cols="12" md="4">
      <v-card style="background-color:#1a1a1a; border:1px solid #2a2a2a;
                     border-radius:0; height:100%; padding:32px;">
        <div style="font-size:5rem; line-height:0.8; color:#E53935;
                    opacity:0.4; font-weight:900; margin-bottom:16px;">"</div>

        <v-card-text style="color:#cccccc; font-size:0.95rem; line-height:1.8;
                            font-weight:300; padding:0; margin-bottom:24px;">
          Up to date equipment with highly trained professionals.
          Awesome facilities — worth every penny!
        </v-card-text>

        <v-rating :length="5" :size="20" :model-value="4"
                  active-color="#E53935" color="#333"
                  style="margin-bottom:20px;"></v-rating>

        <div style="display:flex; align-items:center; gap:12px;">
          <div style="width:44px; height:44px; background:#E53935;
                      display:flex; align-items:center; justify-content:center;
                      font-size:1.2rem; font-weight:800; color:white; flex-shrink:0;">
            D
          </div>
          <div>
            <div style="color:#ffffff; font-weight:600; font-size:0.9rem;">Devon R.</div>
            <div style="color:#666; font-size:0.8rem;">Elite Member</div>
          </div>
        </div>
      </v-card>
    </v-col>

  </v-row>
</v-container>

<!-- CONTACT US -->
<v-container fluid style="background-color:#111111; padding:80px 40px;">
    <v-row justify="center">
        <v-col cols="12" md="4" class="text-center mb-8">
            <div style="
            color:#E53935;
            font-size: 0.75;
            letter-spacing:0.3em;
            font-weight:600;
            margin-bottom:12px;
            text-transform: uppercase;
            ">Get In Touch </div>

            <div style="
            color:#ffffff;
            font-size: 1.8rem;
            font-weight:800;
            text-transform:uppercase;
            margin-bottom:24px;
            ">contact us</div>

            <div style="color:#cccccc;
                        font-size: 0.95rem;
                        margin-bottom:12px;">
             0755550000
            </div>
            <div style="color:#cccccc;
                        font-size: 0.95rem;
                        margin-bottom:12px;">
             macfit@gmail.com
            </div>
        </v-col>

        <!-- Divider -->
        <v-divider vertical color="2a2a2a" class="d-none d-md-flex"></v-divider>

        <!-- Opening hours -->
        <v-col cols="12" md="4" class="text-center mb-8">
            <div style="
                color:#E53935;
                font-size:0.75;
                letter-spacing: 0.3em;
                font-weight:600;
                margin-bottom: 12px;
                text-transform: uppercase;
                ">Operating hours</div>

            <div style="
            color:#ffffff;
            font-size:1.8 rem;
            font-weight:800;
            text-transform:uppercase;
            margin-bottom:24px;
            ">Opening Hours</div>

            <div style="color:#cccccc; font-size: 0.95rem; margin-bottom:8px;">
                Mon - Fri: 5.00am - 9.00pm
            </div>
            <div style="color:#cccccc; font-size: 0.95rem;">
                Sat - Sun: 7.00am - 6.00p.m
            </div>
        </v-col>

        <!-- Divider -->
         <v-divider vertical color="#2a2a2a" class="d-none d-md-flex"></v-divider>

        <!-- Location -->
         <v-col cols="12" md="4" class="text-center mb-8">
            <div style="
                color:#E53935;
                font-size:0.75rem;
                letter-spacing: 0.3em;
                font-weight: 600;
                margin-bottom: 12px;
                text-transform: uppercase;
                ">Find Us</div>

            <div style="
            color:#ffffff;
            font-size:1.8 rem;
            font-weight:800;
            text-transform:uppercase;
            margin-bottom:24px;
            ">Madaraka Plaza</div>

            <div style="color:#cccccc; font-size: 0.95rem; margin-bottom:8px;">
                Madaraka Plaza
            </div>
            <div style="color:#cccccc; font-size: 0.95rem;">
                Opposite Strathmore University
            </div>
        </v-col>
    </v-row>

    <!-- Bottom tagline -->
     <v-row justify="center" class="mt-8">
        <v-col cols="12" class="text-center">
            <v-divider style="border-color:#2a2a2a; margin-bottom:24px;"></v-divider>
            <div style=" color:#E53935;
                        font-size:1.1rem;
                        letter-spacing: 0.2em;
                        font-weight:700;
                        text-transform: uppercase;
                        ">Where Every Body Belongs</div>
            <div style="color:#555; font-size:0.8rem; margin-top:8px">
                2026 MacFit Gym. All rights reserved.
            </div>
        </v-col>
     </v-row>       
</v-container>
</template>