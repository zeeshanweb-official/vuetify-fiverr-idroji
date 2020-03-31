<template>
  <div class="ma-5">
    <v-container class="text-times-new-roman">
      <v-layout row no-gutters justify-center class="bgchnged">
        <v-flex md12 sm12 xs12 class="fixedheeght">
          <v-layout row no-gutters justify-space-between>
            <v-flex md3 sm5 xs12>
              <div id="myprops" class="pt-2 ml-1">MY PROPERTIES</div>
            </v-flex>
            <v-flex md4 sm5 xs12 class="mr-1">
              <v-layout row no-gutters>
                <v-flex md12 xs12>
                  <div class="inputbox">
                    <input type="text" id="fixinput" placeholder="Search" />
                    <div class="btnicon">
                      <svg style="width:43px;height:24px;margin-top:8px" viewBox="0 0 24 24">
                        <path
                          fill="#B9B4B4"
                          d="M9.5,3A6.5,6.5 0 0,1 16,9.5C16,11.11 15.41,12.59 14.44,13.73L14.71,14H15.5L20.5,19L19,20.5L14,15.5V14.71L13.73,14.44C12.59,15.41 11.11,16 9.5,16A6.5,6.5 0 0,1 3,9.5A6.5,6.5 0 0,1 9.5,3M9.5,5C7,5 5,7 5,9.5C5,12 7,14 9.5,14C12,14 14,12 14,9.5C14,7 12,5 9.5,5Z"
                        />
                      </svg>
                    </div>
                  </div>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
      <v-layout row no-gutters justify-center>
        <v-flex sm12 md12>
          <v-card flat>
            <v-layout row no-gutters class="mb-3 ml-5">
              <v-flex sm12 md5 class="mt-4">
                All
                <v-btn
                  class="ml-3 mr-1 smallbtn greenbutton"
                  @click="sortBy('active')"
                  fab
                  dark
                  small
                >
                  <v-icon dark>mdi-chevron-up</v-icon>
                </v-btn>Active
                <v-btn
                  class="ml-3 mr-1 smallbtn redbutton"
                  @click="sortBy('set up')"
                  fab
                  dark
                  small
                >
                  <v-icon dark>mdi-chevron-right</v-icon>
                </v-btn>Set up
                <v-btn class="ml-3 mr-1 smallbtn btnscndry" fab dark small>
                  <v-icon dark>mdi-calendar</v-icon>
                </v-btn>Date
              </v-flex>
            </v-layout>
            <v-divider></v-divider>
            <div v-for="i in properties" class="pa-4" :key="i.index">
              <v-layout row no-gutters wrap>
                <v-flex xs9 sm10 md11>
                  <div class="title-texts">{{i.title}}</div>
                  <div class="text-subtitle gray--text">Address: {{i.address}}</div>
                </v-flex>
                <v-flex xs3 sm2 md1>
                  <div>
                    <v-chip small :class="`white--text ${i.class}`">{{i.status}}</v-chip>
                  </div>
                </v-flex>
              </v-layout>
              <v-divider></v-divider>
            </div>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      properties: [
        {
          title: "Icon Brickell Condo No1",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Mint",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "ACTIVE",
          class: "redactive"
        },
        {
          title: "Icon Brickell Condo No2",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "ACTIVE",
          class: "redactive"
        },
        {
          title: "Hidden Bay",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Icon Brickell Condo No2",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Mint",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "ACTIVE",
          class: "redactive"
        },
        {
          title: "Icon Brickell Condo No1",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "ACTIVE",
          class: "redactive"
        },
        {
          title: "Icon Brickell Condo No2",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Icon Brickell Condo No4",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Icon Brickell Condo No1",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Vuetify",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "ACTIVE",
          class: "redactive"
        }
      ],
      values: [
        {
          title: "Icon Brickell Condo No1",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Mint",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "ACTIVE",
          class: "redactive"
        },
        {
          title: "Icon Brickell Condo No2",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "ACTIVE",
          class: "redactive"
        },
        {
          title: "Hidden Bay",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Icon Brickell Condo No2",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Mint",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "ACTIVE",
          class: "redactive"
        },
        {
          title: "Icon Brickell Condo No1",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "ACTIVE",
          class: "redactive"
        },
        {
          title: "Icon Brickell Condo No2",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Icon Brickell Condo No4",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Icon Brickell Condo No1",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "SET UP",
          class: "setup"
        },
        {
          title: "Vuetify",
          address: "475 Brickell Ave, Miami FL 33131",
          status: "ACTIVE",
          class: "redactive"
        }
      ]
    };
  },
  methods: {
    sortBy(para) {
      let text = para.toUpperCase();
      let newarray = [];
      this.values.map(item => {
        if (item.status === text) {
          newarray.push(item);
        }
      });
      this.properties = newarray;
    }
  }
};
</script>
<style>
.bgchnged {
  background-color: rgb(243, 243, 243);
  height: 100px;
  padding-top: 15px;
}
@media only screen and (max-width: 600px) {
  .bgchnged {
    width: 100vw;
    margin-left: -32px;
    padding-left: 36px;
    padding-right: 35px;
    margin-bottom: 40px;
    padding-top: 34px;
    margin-top: -31px;
  }
}
@media only screen and (min-width: 960px) and (max-width: 1263px) {
  #fixinput {
    width: 80% !important;
  }
}
@media only screen and (max-width: 855px) {
  #fixinput {
    width: 80% !important;
  }
}
#myprops {
  white-space: nowrap;
  text-align: left;
  font-family: "Roboto", sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  color: rgba(33, 150, 243, 1);
  margin-bottom: 15px;
}
.srchicn {
  color: aliceblue;
}
.btnicon {
  display: inline-block;
  width: 39px;
  height: 35px;
  color: white;
}
#fixinput {
  width: 85%;
  height: 105%;
  padding-left: 14px;
  position: relative;
  top: -10px;
}
#fixinput:focus {
  outline: none;
}
.inputbox {
  border: 2px solid lightgray;
  height: 40px;
  border-radius: 5px;
  background-color: white;
}
.btnscndry {
  background-color: gray !important;
}
.text-times-new-roman {
  font-family: "Times New Roman", Times, serif;
}
.setup {
  background-color: rgb(221, 83, 110) !important;
  border-radius: 5px !important;
  font-size: 10px !important;
}
.redactive {
  background-color: rgb(139, 197, 63) !important;
  border-radius: 5px !important;
  font-size: 10px !important;
}
.greenbutton {
  background-color: rgb(139, 197, 63) !important;
}
.redbutton {
  background-color: rgb(221, 83, 110) !important;
}
.smallbtn {
  height: 20px !important;
  width: 20px !important;
}
.greenbutton > .v-btn__content > .v-icon,
.redbutton > .v-btn__content > .v-icon,
.smallbtn > .v-btn__content > .v-icon {
  font-size: 27px !important;
  padding-bottom: 6px !important;
}
.btnscndry > .v-btn__content > .v-icon {
  font-size: 14px !important;
  padding-bottom: 5px !important;
}
.title-texts {
  font-size: 16px !important;
}
.text-subtitle {
  font-size: 12px !important;
}
</style>
  