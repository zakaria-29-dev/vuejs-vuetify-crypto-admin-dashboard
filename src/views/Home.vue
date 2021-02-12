<template>
  <div class="home">
    <v-toolbar class="mt-5" flat>
      <v-toolbar-title>
        <span class="caption">Overview Dashboard></span><br>Tranding View
      </v-toolbar-title>
      <v-app-bar flat color="rgba(0,0,0,0)" class="ml-16">
        <v-tabs v-model="tab" color="purple" slider-size="3">
          <v-tab>
            <v-btn fab color="purpe lighten-4" elevation="0">
              <v-icon color="purple">fab fa-bitcoin</v-icon>
            </v-btn>
          </v-tab>
          <v-tab>
            <v-btn fab color="red lighten-4" elevation="0">
              <v-icon color="red">fas fa-rupee-sign</v-icon>
            </v-btn>
          </v-tab>
          <v-tab>
            <v-btn fab color="blue lighten-4" elevation="0">
              <v-icon color="green">fas fa-yen-sign</v-icon>
            </v-btn>
          </v-tab>
          <v-tab>
            <v-btn fab color="grey lighten-4" elevation="0">
              <v-icon color="grey">fas fa-chevron-right</v-icon>
            </v-btn>
          </v-tab>
        </v-tabs>
      </v-app-bar>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>far fa-bell</v-icon>
      </v-btn>
      <v-badge bordered bottom color="green" dot offset-x="10" offset-y="10">
        <v-avatar size="40">
          <v-img src="https://cdn.vuetifyjs.com/images/lists/2.jpg"></v-img>
        </v-avatar>
      </v-badge>
    </v-toolbar>
    <v-divider></v-divider>
    <v-container class="mt-5">
      <v-row>
        <v-col cols="12" sm="4">
          <v-hover v-slot="{ hover }" open-delay="200">
            <v-card color="cyan darken-1" :elevation="hover ? 16 : 2">
              <v-row>
                <v-col cols="12" sm="8">
                  <v-list-item three-line>
                    <v-list-item-content>
                      <div class="mb-4">
                        <v-btn fab color="cyan lighten-2" elevation="0">
                          <v-icon color="white">fab fa-bitcoin</v-icon>
                        </v-btn>
                      </div>
                      <v-list-item-title class="headline mb-1 white--text">
                        $8520.50
                      </v-list-item-title>
                      <v-list-item-subtitle class="white--text">Market Cap $151.458</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </v-col>
                <v-col cols="12" sm="4">
                  <v-avatar size="100" class="ml-n10 mt-6" tile>
                    <v-img src="wallet.png"></v-img>
                  </v-avatar>
                </v-col>
              </v-row>
            </v-card>
          </v-hover>
        </v-col>
        <v-col cols="12" sm="4">
          <v-hover v-slot="{hover }" open-delay="200">
            <v-card color="pink darken-1" :elevation="hover ? 16 : 2">
              <v-row>
                <v-col cols="12" sm="8">
                  <v-list-item three-line>
                    <v-list-item-content>
                      <div class="mb-4">
                        <v-btn fab color="pink lighten-2" elevation="0">
                          <v-icon color="white">fas fa-rupee-sign</v-icon>
                        </v-btn>
                      </div>
                      <v-list-item-title class="headline mb-1 white--text">
                        $7220.50
                      </v-list-item-title>
                      <v-list-item-subtitle class="white--text">Market Cap $151.458</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </v-col>
                <v-col cols="12" sm="4">
                  <v-avatar size="100" class="ml-n10 mt-6" tile>
                    <v-img src="wallet.png"></v-img>
                  </v-avatar>
                </v-col>
              </v-row>
            </v-card>
          </v-hover>
        </v-col>
        <v-col cols="12" sm="4">
          <v-hover v-slot="{ hover }" open-delay="200">
            <v-card color="orange darken-1" :elevation="hover ? 16 :2">
              <v-row>
                <v-col cols="12" sm="8">
                  <v-list-item three-line>
                    <v-list-item-content>
                      <div class="mb-4">
                        <v-btn fab color="orange lighten-2" elevation="0">
                          <v-icon color="white">fas fa-pound-sign</v-icon>
                        </v-btn>
                      </div>
                      <v-list-item-title class="headline mb-1 white--text">
                        $350.50
                      </v-list-item-title>
                      <v-list-item-subtitle class="white--text">Market Cap $151.458</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </v-col>
                <v-col cols="12" sm="4">
                  <v-avatar size="100" class="ml-n10 mt-6" tile>
                    <v-img src="wallet.png"></v-img>
                  </v-avatar>
                </v-col>
              </v-row>
            </v-card>
          </v-hover>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" sm="6">
          <v-card>
            <v-app-bar flat color="rgba(0,0,0,0)">
              <v-toolbar-title class="title black--text pl-0 ml-2">
                Impression 
              </v-toolbar-title>
              <v-spacer></v-spacer>
              <v-btn color="deep-purple" class="white--text mr-2">Weekly</v-btn>
              <v-btn color="deep-purple lighten-4" class="deep-purple--text ">Monthly</v-btn>
            </v-app-bar>
            <v-sparkline
            :fill="fill"
            :line-width="width"
            :padding="padding"
            :smooth="radius || false"
            :value="value"
            auto-draw
            color="deep-purple"></v-sparkline>
          </v-card>
        </v-col>
        <v-col cols="12" sm="6">
          <v-card>
            <v-app-bar flat color="rgba(0,0,0,0)">
              <v-toolbar-title class="title black--text pl-0 ml-2">
                Activity
              </v-toolbar-title>
            </v-app-bar>
            <v-app-bar flat color="rgba(0,0,0,0)">
              <v-btn fab color="purple lighten-4" elevation="0">
                <v-icon color="purple">fab fa-bitcoin</v-icon>
              </v-btn>
              <v-toolbar-title class="title black--text ml-2">
                Sent Bitcoin <span class="caption"><br>To Bitcoin Address</span>
              </v-toolbar-title>
              <v-spacer></v-spacer>
              <v-toolbar-title class="subtitle-1 black--text ml-2">
                -0.00257 BTC
              </v-toolbar-title>
              <v-icon color="green" class="ml-2">fas fa-long-arrow-alt-up</v-icon>
            </v-app-bar>
             <v-app-bar flat color="rgba(0,0,0,0)">
              <v-btn fab color="green lighten-4" elevation="0">
                <v-icon color="green">fas fa-yen-sign</v-icon>
              </v-btn>
              <v-toolbar-title class="title black--text ml-2">
                Receive Lightcoin <span class="caption"><br>Pending</span>
              </v-toolbar-title>
              <v-spacer></v-spacer>
              <v-toolbar-title class="subtitle-1 black--text ml-2">
                -0.0133643 LTC
              </v-toolbar-title>
              <v-icon color="red" class="ml-2">fas fa-long-arrow-alt-down</v-icon>
            </v-app-bar>
          </v-card>
        </v-col>
        <v-col cols="12" sm="6">
          <v-card height="180px">
            <v-row>
              <v-col cols="12" sm="4">
                <v-list-item three-line>
                  <v-list-item-content>
                    <div class="mb-4">Bitcoin</div>
                    <v-list-item-title class="headline mb-1 black--text">
                      2.5578 BTC
                    </v-list-item-title>
                    <v-list-item-subtitle class="grey--text">$2500 USD</v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
              <v-col cols="12" sm="8">
                <v-sparkline
                :value="value"
                :smooth="radius || false"
                :padding="padding"
                :line-width="width"
                :stroke-linecap="lineCap"
                :fill="fills"
                :type="type"
                :auto-line-width="autoLineWidth"
                auto-draw
                color="red"
                >

                </v-sparkline>
                <v-card-actions class="justify-end">
                  <v-btn text color="green">
                    <v-icon class="mt-n2 pr-2">fas fa-sort-down</v-icon> 8.5
                  </v-btn>
                </v-card-actions>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" sm="6">
          <v-card>
            <v-row>
              <v-col cols="12" sm="6" class="border">
                <v-list-item three-line>
                  <v-list-item-content>
                    <div class="mb-4">Your Portfolio</div>
                    <v-row>
                      <v-col cols="12" sm="6">
                        <v-progress-circular
                        rotate="360"
                        size="100"
                        width="15"
                        value="70"
                        color="teal"
                        >
                        70%
                        </v-progress-circular>
                      </v-col>
                      <v-col cols="12" sm="6">
                        <v-list-item-subtitle class="grey--text mt-8">2.5578 BTC</v-list-item-subtitle>
                        <v-list-item-subtitle class="grey--text">2500 USD</v-list-item-subtitle>
                      </v-col>
                    </v-row>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
              <v-sol cols="12" sm="6" align="center">
                <v-list-item two-line class="mt-10">
                  <v-list-item-content>
                     <v-list-item-title class="headline mb-1 black--text">
                    $8520.50
                  </v-list-item-title>
                  <v-list-item-subtitle class="grey--text">Pending Balance</v-list-item-subtitle>
                  </v-list-item-content>
                 
                </v-list-item>
              </v-sol>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>

export default {
  name: 'Home',
  data: () => ({
     tab: null,
     text: 'center',
     fill: true,
      padding: 8,
      radius: 10,
      value: [0, 2, 5, 9, 5, 10, 3, 5, 0, 0, 1, 8, 2, 9, 0],
      width: 2,
      lineCap: 'round',
      type: 'trend',
      autoLineWidth: false,
      fills: false,
  })
}
</script>
<style lang="sass" scoped>
.v-card.on-hover.theme--dark
  background-color: rgba(#FFF, 0.8)
  >.v-card__text
    color: #000
</style>
<style scoped>
.border {
  border-right: 1px solid grey
}
</style>
