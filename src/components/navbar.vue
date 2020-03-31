<template>
  <div>
    <v-toolbar>
      <v-app-bar app dark class="colorgradiant">
        <v-app-bar-nav-icon
          class="white--text d-sm-block d-xs-block d-md-block d-lg-none d-xl-none"
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>
        <v-toolbar-title>
          <div id="Group_59">
            <svg class="Path_167" viewBox="47.362 149.377 11.904 5.081">
              <path
                fill="rgba(255,255,255,1)"
                id="Path_167"
                d="M 59.26577758789062 149.3767547607422 L 47.36156845092773 149.3767547607422 L 47.36156845092773 154.457763671875 L 55.16867828369141 154.457763671875 L 59.26577758789062 149.3767547607422 Z"
              />
            </svg>
            <svg class="Path_168" viewBox="57.497 180.001 12.376 5.099">
              <path
                fill="rgba(255,255,255,1)"
                id="Path_168"
                d="M 57.49703216552734 185.1000671386719 L 69.87256622314453 185.1000671386719 L 69.87256622314453 180.0009765625 L 61.61251831054688 180.0009765625 L 57.49703216552734 185.1000671386719 Z"
              />
            </svg>
            <svg class="Path_169" viewBox="45.422 149.377 19.17 21.8">
              <path
                fill="rgba(255,255,255,1)"
                id="Path_169"
                d="M 45.42169570922852 167.5368804931641 L 45.42169570922852 171.1767272949219 L 50.31288909912109 171.1767272949219 L 64.59170532226562 153.4986267089844 L 64.59170532226562 149.3767547607422 L 60.09207916259766 149.3767547607422 L 45.42169570922852 167.5368804931641 Z"
              />
            </svg>
          </div>
        </v-toolbar-title>
        <div class="flex-grow-1"></div>
        <template>
          <v-btn icon>
            <v-menu offset-y class="custmenu">
              <template v-slot:activator="{ on }">
                <v-btn icon v-on="on">
                  <v-icon>mdi-bell-circle</v-icon>
                </v-btn>
              </template>
              <div class="scrollbar" id="style-3">
                <v-list class="fixsize" subheader>
                  <v-subheader
                    class="text-uppercase"
                    style="display:flex; color: rgba(33,150,243,1);font-size: 18px; justify-content:space-between"
                  >
                    My Notifications
                    <v-list-item-icon style="margin-right:0px">
                      <div class="flex-grow-1"></div>
                      <v-icon style="font-size: 30px; margin-top: -10px;">mdi-close</v-icon>
                    </v-list-item-icon>
                  </v-subheader>

                  <v-list-item v-for="item in items" :key="item.title" @click>
                    <div class="alertcircle">
                      <v-list-item-icon>
                        <v-icon
                          style="margin-top: 2px; margin-left: 2px; font-size: 20px; color: rgb(139, 197, 63);"
                        >mdi-minus-box</v-icon>
                      </v-list-item-icon>
                    </div>
                    <v-list-item-content class="limit40">
                      <v-list-item-title style="font-size:14px" v-text="item.title"></v-list-item-title>
                      <v-list-item-subtitle
                        style="font-size:12px"
                        class="text--primary"
                        v-text="item.headline"
                      ></v-list-item-subtitle>
                    </v-list-item-content>
                    <v-list-item-icon>
                      <v-list-item-subtitle
                        class="text--gray subheading"
                        style="font-size:12px; margin-top:10px; margin-right:3px"
                        v-text="item.time"
                      ></v-list-item-subtitle>
                      <v-icon
                        class="item-icon-cust-font"
                        :color="item.active ? ' red accent-3 ' : 'grey'"
                        v-text="item.icon"
                      ></v-icon>
                    </v-list-item-icon>
                  </v-list-item>
                </v-list>
              </div>

              <v-divider></v-divider>
            </v-menu>
          </v-btn>
          <v-btn icon>
            <v-icon>mdi-help-circle</v-icon>
          </v-btn>
        </template>
      </v-app-bar>
    </v-toolbar>

    <v-navigation-drawer
      app
      class="extendedwidth d-block d-lg-none d-xl-none"
      style="background-color:rgb(40%, 40%, 40%); width:297px !important;"
      temporary
      v-model="drawer"
      absolute
    >
      <v-list class="pa-1 colorgradiant fixeddirections">
        <v-layout row>
          <v-flex md11></v-flex>
          <v-flex md1>
            <v-icon
              class="d-md-block d-lg-none d-xl-none"
              @click="drawer=!drawer"
              style="font-size: 24px; margin-top: 9px; color: white;
    margin-left: 245px;"
            >mdi-close</v-icon>
          </v-flex>
        </v-layout>
        <v-container>
          <v-layout row>
            <div id="Group_54">
              <svg class="Path_126" viewBox="641.662 114.51 19.133 8.166">
                <path
                  fill="rgba(255,255,255,1)"
                  id="Path_126"
                  d="M 660.7955322265625 114.5101470947266 L 641.6624145507812 114.5101470947266 L 641.6624145507812 122.6765899658203 L 654.21044921875 122.6765899658203 L 660.7955322265625 114.5101470947266 Z"
                />
              </svg>
              <svg class="Path_128" viewBox="639.433 114.51 30.811 35.038">
                <path
                  fill="rgba(255,255,255,1)"
                  id="Path_128"
                  d="M 639.4332885742188 143.6981048583984 L 639.4332885742188 149.5482788085938 L 647.294677734375 149.5482788085938 L 670.244384765625 121.1350402832031 L 670.244384765625 114.5101470947266 L 663.0123291015625 114.5101470947266 L 639.4332885742188 143.6981048583984 Z"
                />
              </svg>
              <svg class="Path_127" viewBox="653.309 149.701 19.891 8.196">
                <path
                  fill="rgba(255,255,255,1)"
                  id="Path_127"
                  d="M 653.3092041015625 157.8963470458984 L 673.1998291015625 157.8963470458984 L 673.1998291015625 149.7008209228516 L 659.923828125 149.7008209228516 L 653.3092041015625 157.8963470458984 Z"
                />
              </svg>
            </div>
            <div id="smart___secure">
              <span>smart • secure</span>
            </div>
          </v-layout>
          <v-layout class="margintop" row justify-center no-gutters>
            <v-list class="mt-5 negetivemargin80px" shaped>
              <v-list-item-group color="primary">
                <v-list-item style="margin-bottom:12px;" v-for="(item, i) in draweritems" :key="i">
                  <v-list-item-content>
                    <v-list-item-title class="btntext" v-text="item"></v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list-item-group>
            </v-list>
          </v-layout>
          <v-layout row justify-center>
            <div class="btncustomised">LOG OUT</div>
          </v-layout>
        </v-container>
      </v-list>
    </v-navigation-drawer>
    <v-navigation-drawer
      app
      class="extendedwidth d-none d-lg-block d-xl-block"
      style="background-color:rgb(40%, 40%, 40%); width:297px !important;"
      temporary
      absolute
    >
      <v-list class="pa-1 colorgradiant fixeddirections">
        <v-layout row>
          <v-flex md10></v-flex>
          <v-flex md2>
            <v-icon
              class="d-md-block d-lg-none d-xl-none"
              @click="drawer=!drawer"
              style="font-size: 24px; margin-top: 9px; color: white;"
            >mdi-close</v-icon>
          </v-flex>
        </v-layout>
        <v-container>
          <v-layout row>
            <div id="Group_54">
              <svg class="Path_126" viewBox="641.662 114.51 19.133 8.166">
                <path
                  fill="rgba(255,255,255,1)"
                  id="Path_126"
                  d="M 660.7955322265625 114.5101470947266 L 641.6624145507812 114.5101470947266 L 641.6624145507812 122.6765899658203 L 654.21044921875 122.6765899658203 L 660.7955322265625 114.5101470947266 Z"
                />
              </svg>
              <svg class="Path_128" viewBox="639.433 114.51 30.811 35.038">
                <path
                  fill="rgba(255,255,255,1)"
                  id="Path_128"
                  d="M 639.4332885742188 143.6981048583984 L 639.4332885742188 149.5482788085938 L 647.294677734375 149.5482788085938 L 670.244384765625 121.1350402832031 L 670.244384765625 114.5101470947266 L 663.0123291015625 114.5101470947266 L 639.4332885742188 143.6981048583984 Z"
                />
              </svg>
              <svg class="Path_127" viewBox="653.309 149.701 19.891 8.196">
                <path
                  fill="rgba(255,255,255,1)"
                  id="Path_127"
                  d="M 653.3092041015625 157.8963470458984 L 673.1998291015625 157.8963470458984 L 673.1998291015625 149.7008209228516 L 659.923828125 149.7008209228516 L 653.3092041015625 157.8963470458984 Z"
                />
              </svg>
            </div>
            <div id="smart___secure">
              <span>smart • secure</span>
            </div>
          </v-layout>
          <v-layout class="margintop" row justify-center no-gutters>
            <v-list class="mt-5 negetivemargin80px" shaped>
              <v-list-item-group color="primary">
                <v-list-item style="margin-bottom:12px;" v-for="(item, i) in draweritems" :key="i">
                  <v-list-item-content>
                    <v-list-item-title class="btntext" v-text="item"></v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list-item-group>
            </v-list>
          </v-layout>
          <v-layout row justify-center>
            <div class="btncustomised">LOG OUT</div>
          </v-layout>
        </v-container>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      routes: [
        { title: "Dashboard", icon: "mdi-view-dashboard" },
        { title: "Photos", icon: "mdi-image" },
        { title: "About", icon: "mdi-help-box" }
      ],
      items: [
        {
          active: true,
          title: "Zeeshan",
          icon: "mdi-alert-circle",
          headline: "send you a message ",
          time: "21 minnutes "
        },
        {
          active: true,
          title: "Ranee Carlson",
          icon: " ",
          headline: "send you a new offer ",
          time: "51 minutes "
        },
        {
          title: "Transaction Failed",
          icon: "",
          headline: "Transaction ID 27081996",
          time: "23 hours"
        },
        {
          title: "Your Password is Changed",
          icon: "",
          headline: "",
          time: "11 days"
        },
        {
          active: true,
          title: "Zeeshan",
          icon: "mdi-alert-circle",
          headline: "send you a message ",
          time: "21 minnutes "
        }
      ],
      draweritems: [
        "Profile",
        "Applications",
        "Properties",
        "Bank Accounts",
        "Reports"
      ],

      drawer: false,
      right: null
    };
  }
};
</script>
<style>
.custmenu {
  left: 1000px !important;
}
.scrollbar {
  float: left;
  height: 300px;
  width: 300px;
  background: #f5f5f5;
  overflow-y: scroll;
  margin-bottom: 25px;
}

#style-3::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  background-color: #f5f5f5;
}

#style-3::-webkit-scrollbar {
  width: 6px;
  background-color: #f5f5f5;
}

#style-3::-webkit-scrollbar-thumb {
  background-color: #000000;
}

.mrgin-left-adjust {
  margin-left: -10px;
}
@import url("https://fonts.googleapis.com/css?family=Roboto&display=swap");
.btncustomised {
  background-color: rgb(55%, 77%, 25%);
  width: 187px;
  height: 64px;
  padding-top: 21px;
  color: white;
  text-align: center;
  margin-top: 50px;
}
.margintop {
  margin-top: 75px;
}
.btntext {
  font-size: 20px !important;
  color: rgba(255, 255, 255, 1);
}
.negetivemargin80px {
  margin-left: -50px;
}
#smart___secure {
  position: relative;
  left: 16px;
  top: 62px;
  overflow: visible;
  width: 117px;
  white-space: nowrap;
  line-height: 13px;
  margin-top: -1.5px;
  text-align: left;
  font-family: "Roboto", sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 10px;
  color: rgba(255, 255, 255, 1);
  letter-spacing: 4px;
}
#Group_54 {
  width: 30.811px;
  height: 35.038px;
  left: 48.002px;
  top: 0px;
  overflow: visible;
  position: relative;
}
.Path_126 {
  overflow: visible;
  position: relative;
  top: 15px;
  left: 1px;
  width: 19.134px;
  height: 8.167px;
  transform: matrix(1, 0, 0, 1, 0, 0);
}
.Path_127 {
  overflow: visible;
  position: relative;
  left: 10px;
  top: -24.159px;
  width: 19.891px;
  height: 8.196px;
  transform: matrix(1, 0, 0, 1, 0, 0);
}
.Path_128 {
  overflow: visible;
  position: relative;
  top: 0px;
  left: -1px;
  width: 30.811px;
  height: 35.038px;
  transform: matrix(1, 0, 0, 1, 0, 0);
}
.extendedwidth {
  width: 410px !important;
  height: 845px !important;
}
.fixeddirections {
  width: 297px;

  height: 845px !important;
  overflow: hidden;
}
.colorgradiant {
  background: rgb(25, 20, 124);
  background: linear-gradient(
    17deg,
    rgba(25, 20, 124, 1) 0%,
    rgba(94, 55, 147, 1) 80%,
    rgba(172, 53, 218, 1) 100%
  ) !important;
}
@media only screen and (max-width: 400px) {
  .v-menu__content--fixed.menuable__content__active {
    left: 0% !important;
    width: 100% !important;
    min-width: 100% !important;
  }
  .fixsize {
    width: 100% !important;
    max-width: 100% !important;
    margin-top: 45px;
  }
}
.item-icon-cust-font {
  font-size: 32px !important;
}
.fixsize {
  max-width: 330px;
}
.limit40 {
}
.alertcircle {
  border: 1px solid black;
  max-width: 40px;
  max-height: 40px;
  border-radius: 40px;
  padding-left: 1px;
  padding-bottom: 10px;
  margin-right: 10px;
  border-color: rgb(170, 207, 121);
}
.alertcircle > .v-list-item__icon {
  margin: 7px;
}
.iconcntr {
  margin-left: 25px;
}
.Path_167 {
  overflow: visible;
  position: absolute;
  top: 0px;
  left: 1.058px;
  width: 11.904px;
  height: 5.081px;
  transform: matrix(1, 0, 0, 1, 0, 0);
}
.Path_168 {
  overflow: visible;
  position: absolute;
  top: 16.7px;
  left: 6.585px;
  width: 12.376px;
  height: 5.099px;
  transform: matrix(1, 0, 0, 1, 0, 0);
}
.Path_169 {
  overflow: visible;
  position: absolute;
  top: 0px;
  left: 0px;
  width: 19.17px;
  height: 21.8px;
  transform: matrix(1, 0, 0, 1, 0, 0);
}
#Group_59 {
  opacity: 0.454;
  position: absolute;
  width: 19.17px;
  height: 21.8px;
  left: 50px;
  top: 22px;
  overflow: visible;
}
</style>
