<template>
  <v-container class="txt">
    <v-flex>
      <v-card class="mx-auto text-center" color="#26314C" dark>
        <v-card-title class="white--text display-1  text-uppercase">
          My Stats
        </v-card-title>
        <v-sparkline
          :value="sparklineData"
          padding="18"
          label-size="4"
          color="cyan"
          :gradient="['#007bff', 'cyan']"
          :line-width="1"
          :stroke-linecap="'round'"
        >
        </v-sparkline>
      </v-card>
    </v-flex>

    <v-layout row class="mt-2">
      <v-flex class="pa-2" md4 sm12>
        <v-card color="#26314C" height="100">
          <v-layout row justify-space-between class="ma-0">
            <v-flex md12 class="vl" >
              <div class="pa-6">
                <div class="headline font-weight-thin white--text">Earnings</div>
                <div class="font-weight-thin white--text"> Ksh 1234</div>
              </div>
            </v-flex>
            
          </v-layout>
        </v-card>
      </v-flex>
      <v-flex class="pa-2" md4 sm12>
        <v-card color="#26314C" height="100">
          <v-layout row justify-space-between class="ma-0">
           <v-flex md12 class="vl" >
              
              <div class="pa-6">
                <div class="headline font-weight-thin white--text">Expenses</div>
                <div class="font-weight-thin white--text"> Ksh 1234</div>
              </div>
            </v-flex>
            <v-flex xs3>
              <v-icon class="ma-4" color="#ff8133" size="65">> mdi-cash-minus</v-icon>
            </v-flex>
          </v-layout>
        </v-card>
      </v-flex>
      <v-flex class="pa-2" md4 xs12>
        <v-card color="#26314C" height="100">
          <v-layout row justify-space-between class="ma-0">
            <v-flex md12 class="vl" >
              <div class="pa-6">
                <div class="headline font-weight-thin white--text">Net</div>
                <div class="font-weight-thin white--text"> 4</div>
              </div>
            </v-flex>
            
          </v-layout>
        </v-card>
      </v-flex>
    </v-layout>
    <v-layout row class="mt-2">
      <v-flex class="pa-2" md6 sm12>
        <v-card class="card-one">
          <v-layout row justify-space-between class="ma-0">
            <v-flex xs9 >
              <div class="pa-6">
                <div class="headline font-weight-thin white--text">Mpesa Shares</div>
                <div class="font-weight-thin white--text"> 441,234</div>
              </div>
            </v-flex>
            <v-flex xs3>
              <v-icon class="ma-4" color="#ff8133" size="65">> mdi-cash-plus</v-icon>
            </v-flex>
          </v-layout>
        </v-card>
      </v-flex>
      <v-flex class="pa-2" md6 sm12>
        <v-card class="card-one">
         <v-layout row justify-space-between class="ma-0">
            <v-flex xs9 >
              <div class="pa-6">
                <div class="headline font-weight-thin white--text">Referers</div>
                <div class="font-weight-thin white--text">34</div>
              </div>
            </v-flex>
            <v-flex xs3>
              <v-icon class="ma-4" color="#ff8133" size="65">> mdi-notebook-edit</v-icon>
            </v-flex>
          </v-layout>
        </v-card>
      </v-flex>
    </v-layout>

    <v-layout row>
      <v-flex class="pa-2" md6 sm12>
        <v-card elevation="24" color="#26314C" height="100%">
          <v-toolbar dark color="#202941" class="mb-4">
            <v-toolbar-title>Mpesa Auction</v-toolbar-title>
          </v-toolbar>
          <v-row>
            >
            <v-card-text class="white--text">
              <div class="text-center">
                <no-ssr>
                  <flip-countdown
                    deadline="2021-02-25 00:00:00 "
                    :showDays="false"
                  ></flip-countdown>
                </no-ssr>
                <h2 class="card-title font-weight-bold mt-4">
                  Left To Open Bid
                </h2>
              </div>
            </v-card-text>
          </v-row>
        </v-card>
      </v-flex>
      <v-flex md6 xs 12 class="pa-2">
        <v-card elevation="24" class="card-one mb-4">
          <v-toolbar dark color="#202941">
            <v-toolbar-title>Outgoing</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-chip class="ma-2" color="primary">
              Outgoing share by status
            </v-chip>
          </v-toolbar>

          <v-row class="white--text" align="center">
            <v-flex>
              <v-progress-circular
                :rotate="-90"
                :size="100"
                :width="15"
                :value="value"
                color="primary"
                class="ml-12 mt-6"
              >
                {{ value }}
              </v-progress-circular></v-flex
            >
            <v-flex>
              <v-row class="mt-4"
                ><div class="hr mt-2 success"></div>
                <span class="ml-4"> 0% Confirmed</span>
              </v-row>

              <v-row
                ><div class="hr mt-2 warning"></div>
                <span class="ml-4"> 0% Paired</span>
              </v-row>
              <v-row
                ><div class="hr mt-2 info"></div>
                <span class="ml-4"> 99% Pending</span>
              </v-row></v-flex
            >
          </v-row>
        </v-card>

        <v-card elevation="24" class="card-one">
          <v-toolbar dark color="#202941">
            <v-toolbar-title>Incoming</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-chip class="ma-2" color="primary">
              Incoming share by status
            </v-chip>
          </v-toolbar>
          <v-row class="white--text" align="center">
            <v-flex>
              <v-progress-circular
                :rotate="-90"
                :size="100"
                :width="15"
                :value="value"
                color="primary"
                class="ml-12 mt-6"
              >
                {{ value }}
              </v-progress-circular></v-flex
            >
            <v-col cols="6">
              <v-row class="mt-4"
                ><div class="hr mt-2 success"></div>
                <span class="ml-4"> 0% Confirmed</span>
              </v-row>

              <v-row
                ><div class="hr mt-2 warning"></div>
                <span class="ml-4"> 0% Paired</span>
              </v-row>
              <v-row
                ><div class="hr mt-2 info"></div>
                <span class="ml-4"> 99% Pending</span>
              </v-row></v-col
            >
          </v-row>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";
import FlipCountdown from "vue2-flip-countdown";

export default {
  components: {
    Logo,
    VuetifyLogo,
    FlipCountdown,
  },

  data() {
    return {
      interval: {},
      labels: ["12am", "3am", "6am", "9am", "12pm", "3pm", "6pm", "9pm"],
      value: 99,
      sparklineData: [423, 446, 675, 510, 590, 610, 423],
    };
  },
};
</script>
<style scoped lang="scss">
.btn {
  color: #fff;
}
.card-one {
  height: 200px;

  background-color: #26314c;
}
.vl {
  border-left: 6px solid cyan;
  height: 100px;
}
.hr {
  border-bottom: 8px solid;
  width: 1.5rem;
  height: 0.45rem;
  border-radius: 1.1rem;
}
.digit {
  color: #ecf0f1;
  font-size: 130px;
  font-weight: 100;
  margin: 10px;
  text-align: center;
}
.block {
  display: flex;
  flex-direction: column;
  margin: 20px;
}
.countdown {
  display: flex;
}
.v-sheet--offset {
  top: -17px;
  position: relative;
}
.stats {
  width: 100%;
  height: 200px;
}
.txt{
  font-family: 'PT Sans', sans-serif;
}
</style>
