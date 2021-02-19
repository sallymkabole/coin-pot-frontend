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
              :width="15"
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
          <v-toolbar dark color="#202941" class="mb-4">
            <v-toolbar-title>Mpesa Auction</v-toolbar-title>
          </v-toolbar>
          <v-row>
            <v-col cols="6">
              <v-card-text class="white--text mt-12">
                <h2 class="card-title font-weight-bold mt-2 ml-2">
                  Time Left To Open Bid
                </h2>

                <p class="d-inline-flex font-weight-bold ml-2 mt-1">
                  {{ formattedTimeLeft }}
                </p>
              </v-card-text>
            </v-col>
            <v-col cols="6"
              ><div class="base-timer">
                <svg
                  class="base-timer__svg"
                  viewBox="0 0 100 100"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <g class="base-timer__circle">
                    <circle
                      class="base-timer__path-elapsed"
                      cx="50"
                      cy="50"
                      r="45"
                    ></circle>
                    <path
                      :stroke-dasharray="circleDasharray"
                      class="base-timer__path-remaining"
                      :class="remainingPathColor"
                      d="
            M 50, 50
            m -45, 0
            a 45,45 0 1,0 90,0
            a 45,45 0 1,0 -90,0
          "
                    ></path>
                  </g>
                </svg>
                <span class="base-timer__label">{{ formattedTimeLeft }}</span>
              </div></v-col
            >
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";
const FULL_DASH_ARRAY = 283;
const WARNING_THRESHOLD = 10;
const ALERT_THRESHOLD = 5;

const COLOR_CODES = {
  info: {
    color: "green",
  },
  warning: {
    color: "orange",
    threshold: WARNING_THRESHOLD,
  },
  alert: {
    color: "red",
    threshold: ALERT_THRESHOLD,
  },
};

const TIME_LIMIT = 6000;
export default {
  components: {
    Logo,
    VuetifyLogo,
  },
  data() {
    return {
      timePassed: 0,
      timerInterval: null,
      interval: {},
        value: 0,
    };

  },
  beforeDestroy () {
      clearInterval(this.interval)
    },

  computed: {
    circleDasharray() {
      return `${(this.timeFraction * FULL_DASH_ARRAY).toFixed(0)} 283`;
    },

    formattedTimeLeft() {
      const timeLeft = this.timeLeft;
      const minutes = Math.floor(timeLeft / 60);
      let seconds = timeLeft % 60;

      if (seconds < 10) {
        seconds = `0${seconds}`;
      }

      return `${minutes}:${seconds}`;
    },

    timeLeft() {
      return TIME_LIMIT - this.timePassed;
    },

    timeFraction() {
      const rawTimeFraction = this.timeLeft / TIME_LIMIT;
      return rawTimeFraction - (1 / TIME_LIMIT) * (1 - rawTimeFraction);
    },

    remainingPathColor() {
      const { alert, warning, info } = COLOR_CODES;

      if (this.timeLeft <= alert.threshold) {
        return alert.color;
      } else if (this.timeLeft <= warning.threshold) {
        return warning.color;
      } else {
        return info.color;
      }
    },
  },

  watch: {
    timeLeft(newValue) {
      if (newValue === 0) {
        this.onTimesUp();
      }
    },
  },

  mounted() {
    this.startTimer();
    this.interval = setInterval(() => {
        if (this.value === 100) {
          return (this.value = 0)
        }
        this.value += 10
      }, 1000)
  },

  methods: {
    onTimesUp() {
      clearInterval(this.timerInterval);
    },

    startTimer() {
      this.timerInterval = setInterval(() => (this.timePassed += 1), 1000);
    },
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
.base-timer {
  position: relative;
  width: 300px;
  height: 300px;

  &__svg {
    transform: scaleX(-1);
  }

  &__circle {
    fill: none;
    stroke: none;
  }

  &__path-elapsed {
    stroke-width: 7px;
    stroke: grey;
  }

  &__path-remaining {
    stroke-width: 7px;
    stroke-linecap: round;
    transform: rotate(90deg);
    transform-origin: center;
    transition: 1s linear all;
    fill-rule: nonzero;
    stroke: currentColor;

    &.green {
      color: rgb(65, 184, 131);
    }

    &.orange {
      color: orange;
    }

    &.red {
      color: red;
    }
  }

  &__label {
    position: absolute;
    width: 300px;
    height: 300px;
    top: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 48px;
  }
}
</style>
