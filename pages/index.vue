<template>
  <v-container fluid>
    <v-row class="mt-2">
      <v-col cols="12">
        <v-card color="#26314C" height="100">
          <v-row>
            <v-col cols="3">
              <v-card-actions>
                <v-list-item class="grow">
                  <v-list-item-avatar color="#ff8133">
                    <v-icon class="mr-1 white--text"> mdi-cash-plus </v-icon>
                  </v-list-item-avatar>

                  <v-list-item-content>
                    <v-list-item-title class="font-weight-bold white--text">
                      Earnings
                    </v-list-item-title>
                    <v-list-item-subtitle class="white--text"
                      >256</v-list-item-subtitle
                    >
                  </v-list-item-content>

                  <v-row align="center" justify="end">
                    <div class="vl ml-12"></div>
                  </v-row>
                </v-list-item>
              </v-card-actions>
            </v-col>
            <v-col cols="3">
              <v-card-actions>
                <v-list-item class="grow">
                  <v-list-item-avatar color="#ff8133">
                    <v-icon class="mr-1 white--text"> mdi-account </v-icon>
                  </v-list-item-avatar>

                  <v-list-item-content>
                    <v-list-item-title class="font-weight-bold white--text">
                      Expenses
                    </v-list-item-title>
                    <v-list-item-subtitle class="white--text"
                      >256</v-list-item-subtitle
                    >
                  </v-list-item-content>

                  <v-row align="center" justify="end">
                    <div class="vl ml-12"></div>
                  </v-row>
                </v-list-item>
              </v-card-actions>
            </v-col>
            <v-col cols="3">
              <v-card-actions>
                <v-list-item class="grow">
                  <v-list-item-avatar color="#ff8133">
                    <v-icon class="mr-1 white--text"> mdi-account </v-icon>
                  </v-list-item-avatar>

                  <v-list-item-content>
                    <v-list-item-title class="font-weight-bold white--text">
                      Net
                    </v-list-item-title>
                    <v-list-item-subtitle class="white--text"
                      >6</v-list-item-subtitle
                    >
                  </v-list-item-content>

                  <v-row align="center" justify="end">
                    <div class="vl ml-12"></div>
                  </v-row>
                </v-list-item>
              </v-card-actions>
            </v-col>
            <v-col cols="3">
              <v-card-actions>
                <v-list-item class="grow">
                  <v-list-item-avatar color="#ff8133">
                    <v-icon class="mr-1 white--text"> mdi-account </v-icon>
                  </v-list-item-avatar>

                  <v-list-item-content>
                    <v-list-item-title class="font-weight-bold white--text">
                      Referrers
                    </v-list-item-title>
                    <v-list-item-subtitle class="white--text"
                      >0</v-list-item-subtitle
                    >
                  </v-list-item-content>

                  <v-row align="center" justify="end"> </v-row>
                </v-list-item>
              </v-card-actions>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="3">
        <v-card class="card-one">
          <v-card-text class="card-one white--text">
            <h2 class="card-title font-weight-bold mt-2 ml-2">Referrers</h2>

            <p class="d-inline-flex font-weight-bold ml-2 mt-1">Ksh 250</p>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="3">
        <v-card class="card-one">
          <v-card-text class="white--text">
            <h2 class="card-title font-weight-bold mt-2 ml-2">Expenses</h2>

            <p class="d-inline-flex font-weight-bold ml-2 mt-1">Ksh 250</p>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="3">
        <v-card class="card-one">
          <v-card-text class="white--text">
            <h2 class="card-title font-weight-bold mt-2 ml-2">Net</h2>

            <p class="d-inline-flex font-weight-bold ml-2 mt-1">0</p>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="3">
        <v-card class="card-one">
          <v-card-text class="white--text">
            <h2 class="card-title font-weight-bold mt-2 ml-2">Referrers</h2>

            <p class="d-inline-flex font-weight-bold ml-2 mt-1">0</p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="6">
        <v-card elevation="24" class="card-one mb-4">
          <v-toolbar dark color="#202941">
            <v-toolbar-title>Outgoing</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-chip class="ma-2" color="primary">
              Outgoing share by status
            </v-chip>
          </v-toolbar>
          <v-card-text class="white--text">
            <v-progress-circular
              :rotate="-90"
              :size="100"
              :width="15"
              :value="value"
              color="primary"
            >
              {{ value }}
            </v-progress-circular>
          </v-card-text>
        </v-card>
        <v-card elevation="24" class="card-one">
          <v-toolbar dark color="#202941">
            <v-toolbar-title>Incoming</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-chip class="ma-2" color="primary">
              Incoming share by status
            </v-chip>
          </v-toolbar>
          <v-card-text class="white--text">
            <v-progress-circular
              :rotate="-90"
              :size="100"
              :value="value"
              color="primary"
            >
              {{ value }}
            </v-progress-circular>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="6">
        <v-card elevation="24" color="#26314C" height="100%">
          <v-toolbar dark color="#202941" class="mb-4 ">
            <v-toolbar-title >Mpesa Auction</v-toolbar-title>
          </v-toolbar>
          <v-row>
            <v-col cols="12">
              <v-card-text class="white--text">
                

               <div class="text-center">
                 
                  <no-ssr>
                    <flip-countdown
                      deadline="2021-02-25 00:00:00 " :showDays="false"
                    ></flip-countdown>
                  </no-ssr>
                  <h2 class="card-title font-weight-bold mt-4">
                  Left To Open Bid
                </h2>
                </div>
              </v-card-text>
            </v-col>
            
          </v-row>
        </v-card>
      </v-col>
    </v-row>
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
      value: 0,
    };
  },
};
</script>
<style scoped lang="scss">
.btn {
  color: #ff8133;
}
.card-one {
  height: 200px;

  background-color: #26314c;
}
.vl {
  border-left: 6px solid #161d31;
  height: 50px;
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
</style>
