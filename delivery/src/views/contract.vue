<template>
  <div>
    <v-container fluid class="lightgraybg textblue">
      <v-layout row no-gutters>
        <v-flex md1 sm1 xs1 :class="{'text-center': $vuetify.breakpoint.smAndUp}">
          <v-icon class="absicon3">mdi-arrow-left</v-icon>
        </v-flex>
        <v-flex md-4 sm8 xs11>
          <strong>MY SMART CONTRACTS SETUP</strong>
        </v-flex>
      </v-layout>
    </v-container>
    <v-container fluid class="lightgraybg">
      <v-layout row justify-center>
        <v-flex xs10 sm10 md11 lg11 xl11>
          <p class="custome-text" style="margin-bottom:2px">Icon Brickell Condo No1</p>
          <div class="caption" style="margin-top:0px; line-height:1px">Property Name</div>
          <v-card class="mt-5 pa-2" style="margin-bottom:50px;">
            <v-layout row no-gutters wrap>
              <v-flex md12>
                <div class="caption gray--text">
                  <div class="firstSection">
                    <img src="../assets/icons8-money-bill-wave-50.png" alt />
                    <p class="non-ref">NON-REFUNDABLE</p>
                  </div>
                  <v-divider></v-divider>
                  <div class="secondSection">
                    <v-row>
                      <v-col cols="12" sm="12">
                        <p class="mb-0">Type of application</p>

                        <v-select
                          v-model="select"
                          class="custom pa-1 custinput"
                          :items="items"
                          :rules="[v => !!v || 'Item is required']"
                          label="Lease"
                          solo
                        ></v-select>
                        <p class="mb-0">Description</p>

                        <v-select
                          v-model="select"
                          class="custom pa-1 custinput"
                          :items="items"
                          :rules="[v => !!v || 'Item is required']"
                          label="Elevator"
                          solo
                        ></v-select>
                        <p class="mb-0">Amount</p>
                        <v-text-field class="custom bgchangedtogray" value="150" type="text"></v-text-field>
                        <p class="mb-0">Bank account</p>
                        <div class="text-center">
                          <v-layout row justify-center no-gutters>
                            <v-flex lg4>
                              <v-btn
                                class="bankaccountButton d-none d-lg-flex d-xl-block"
                              >Assign New Bank Account</v-btn>
                            </v-flex>
                          </v-layout>
                          <v-btn
                            class="bankaccountButton d-sm-block d-md-flex d-lg-none"
                            block
                          >Assign New Bank Account</v-btn>
                        </div>
                        <p class="mb-0">Deployment Date</p>

                        <v-dialog ref="dialog" persistent width="290px">
                          <template v-slot:activator="{ on }">
                            <v-text-field
                              label="May 18 2019"
                              readonly
                              v-on="on"
                              class="custom bgchangedtogray"
                            ></v-text-field>
                          </template>
                          <v-date-picker v-model="date" scrollable>
                            <div class="flex-grow-1"></div>
                            <v-btn text color="primary" @click="$refs.dialog.save(date)">Cancel</v-btn>
                            <v-btn text color="primary" @click="$refs.dialog.save(date)">OK</v-btn>
                          </v-date-picker>
                        </v-dialog>
                      </v-col>
                    </v-row>
                  </div>
                </div>
              </v-flex>
            </v-layout>
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
      items: ["Lease", "Role2", "role3"]
    };
  }
};
</script>
<style>
.bankaccountButton {
  background-color: rgb(13%, 59%, 95%) !important;
}
.bgchangedtogray {
  background-color: rgb(95%, 95%, 95%) !important;
  padding-left: 15px;
}
.custinput {
  margin: 0px !important;
  margin-bottom: 15px !important;
}
.custinput > .v-input__control {
  height: 30px;
}
.custinput > .v-input__control > .v-input__slot {
  background-color: rgb(95%, 95%, 95%) !important;
  border-radius: 2px;
}
.firstSection {
  margin-bottom: 7px;
}
.firstSection > img {
  width: 26px;
  position: relative;
  top: 8px;
  margin-right: 10px;
}
.non-ref {
  display: inline;
  text-align: left;
  font-family: "Roboto", sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  color: rgba(129, 185, 55, 1);
}
.whitebg {
  background-color: rgb(255, 255, 255);
  margin-top: 15px;
}
.custome-text {
  white-space: nowrap;
  text-align: left;
  font-family: "Roboto", sans-serif;
  font-style: normal;
  font-weight: bold;
  font-size: 20px;
  color: rgba(55, 48, 65, 1);
}
.lightgraybg {
  background-color: #e5e5e5;
}
.lightgraybg:nth-child(1) {
  border-bottom: 1px solid rgb(216, 215, 215);
}
.textblue {
  white-space: nowrap;
  text-align: left;
  font-family: "Roboto", sans-serif;
  font-style: normal;
  font-weight: lighter;
  font-size: 16px;
  color: rgba(33, 150, 243, 1);
}
.absicon3 {
  color: rgb(170, 207, 121) !important;
}
</style>