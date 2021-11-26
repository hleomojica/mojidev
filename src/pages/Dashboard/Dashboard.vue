<template>
  <div class="dashboard-page">
    <!-- Social media -->
    <b-row class="d-md-none">
      <b-col sm="12">
        <div class="effect egeon">
          <div class="buttons">
            <a
              href="https://github.com/hleomojica/"
              target="_blank"
              rel="noopener"
              class="github"
              title="Github"
              ><i class="fa fa-github" aria-hidden="true"></i
            ></a>
            <a
              href="https://linkedin.com/in/hleomojica"
              rel="noopener"
              class="in"
              target="_blank"
              title="Join us on Linked In"
              ><i class="fa fa-linkedin" aria-hidden="true" rel="noopener"></i
            ></a>
            <a href="#" class="fb" title="Join us on Facebook" rel="noopener"
              ><i class="fa fa-facebook" aria-hidden="true"></i
            ></a>

            <a href="#" class="tw" title="Join us on Twitter" rel="noopener"
              ><i class="fa fa-twitter" aria-hidden="true"></i
            ></a>
          </div>
        </div>
      </b-col>
    </b-row>
    <!-- About Card -->
    <b-row>
      <b-col lg="12" md="12" sm="12" xs="12" class="">
        <Card />
      </b-col>
    </b-row>
    <!-- skills section -->
    <b-row>
      <hr />
      <b-col lg="4" md="4" sm="12" xs="12" class="text-center pb-2 pb-2">
        <b-card
          border-variant="secondary"
          header="Skills"
          header-border-variant="secondary"
          align="center"
        >
          <b-card-text
            ><a href="https://vuejs.org/" target="_blank" title="VueJs">
              <img src="../../../public/vue.svg" class="logo-tech vue" />
            </a>
            <a href="https://www.mysql.com/" target="_blank" title="Mysql">
              <img src="../../../public/mysql.svg" class="logo-tech" />
            </a>
            <a href="https://www.php.net/" target="_blank" title="PHP">
              <img src="../../../public/php.svg" class="logo-tech" /> </a
          ></b-card-text>
        </b-card>
      </b-col>
      <b-col lg="4" md="4" sm="12" xs="12" class="text-center pb-2">
        <b-card
          border-variant="secondary"
          header="Education"
          header-border-variant="secondary"
          align="center"
        >
          <b-card-text>
            <h5>Bachelor in systems engineering</h5>
          </b-card-text>
        </b-card>
      </b-col>
      <b-col lg="4" md="4" sm="12" xs="12" class="text-center pb-2">
        <b-card
          border-variant="secondary"
          header="Skills"
          header-border-variant="secondary"
          align="center"
        >
          <b-card-text
            >Lorem ipsum dolor sit amet, consectetur adipiscing
            elit.</b-card-text
          >
        </b-card>
      </b-col>
    </b-row>
    <!-- Projects section -->
    <b-row>
      <b-col md="12">
        <Widget
          title="<h5>Proyectos  <span class='fw-semi-bold'>Recientes</span></h5>"
          customHeader
        >

        <b-row>
          <!-- Project 1  -->
          <b-col md="4" sm="12">
            <b-card
              border-variant="default"
              header="OpemApp"
              header-bg-variant="secondary"
              header-text-variant="white"
              align="center"
              title="Bookings"
              tag="article"
              style="max-width: auto"
              class="mb-5 mt-2"
            >
              <br />
              <b-card-text>
                Here's a blank template to get started: To avoid retyping too
                much info. Do a search and replace with your text editor for the
                following
              </b-card-text>
              <b-list-group flush>
                <b-list-group-item></b-list-group-item>

                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle
                  >Stack
                </b-list-group-item>
                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle
                  >Status
                </b-list-group-item>
                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle
                  >Spotify Family
                </b-list-group-item>
                <b-list-group-item></b-list-group-item>
              </b-list-group>
              <br />
              <b-button v-b-modal.modal-2 variant="secondary"
                >More info</b-button
              >
              <br />
            </b-card>
          </b-col>
          <!-- Project 1  -->
          <b-col md="4">
            <b-card
              border-variant="default"
              header="OpemApp"
              header-bg-variant="secondary"
              header-text-variant="white"
              align="center"
              title="Bookings"
              tag="article"
              style="max-width: auto"
              class="mb-5 mt-2"
            >
              <br />
              <b-card-text>
                Here's a blank template to get started: To avoid retyping too
                much info. Do a search and replace with your text editor for the
                following
              </b-card-text>
              <b-list-group flush>
                <b-list-group-item></b-list-group-item>

                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle
                  >Stack
                </b-list-group-item>
                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle
                  >Status
                </b-list-group-item>
                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle
                  >Spotify Family
                </b-list-group-item>
                <b-list-group-item></b-list-group-item>
              </b-list-group>
              <br />
              <b-button v-b-modal.modal-2 variant="secondary"
                >More info</b-button
              >
              <br />
            </b-card>
          </b-col>
          <!-- Project 1  -->
          <b-col md="4">
            <b-card
              border-variant="default"
              header="OpemApp"
              header-bg-variant="secondary"
              header-text-variant="white"
              align="center"
              title="Bookings"
              tag="article"
              style="max-width: auto"
              class="mb-5 mt-2"
            >
              <br />
              <b-card-text>
                Here's a blank template to get started: To avoid retyping too
                much info. Do a search and replace with your text editor for the
                following
              </b-card-text>
              <b-list-group flush>
                <b-list-group-item></b-list-group-item>

                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle
                  >Stack
                </b-list-group-item>
                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle
                  >Status
                </b-list-group-item>
                <b-list-group-item>
                  <b-icon-x-circle class="h5 mr-2 mb-0 mt-0"></b-icon-x-circle
                  >Spotify Family
                </b-list-group-item>
                <b-list-group-item></b-list-group-item>
              </b-list-group>
              <br />
              <b-button v-b-modal.modal-2 variant="secondary"
                >More info</b-button
              >
              <br />
            </b-card>
          </b-col>
        </b-row>

        </Widget>
      </b-col>
    </b-row>
    <b-row>
      <b-col xs="12">
        <Widget customHeader>
          <div id="avatar">
            <img src="../../assets/dev2.svg" alt="" />
          </div>
        </Widget>
      </b-col>
    </b-row>
    <b-row>
      <b-col xs="12">
        <Widget customHeader>
          <div id="avatar">
            <img src="../../assets/dev2.svg" alt="" />
          </div>
        </Widget>
      </b-col>
    </b-row>
    <b-row>
      <b-col xs="12">
        <div class="h-100">
          <Widget
            class="h-100"
            title="<h6>“Without music, life would be a mistake.”  <span class='fw-semi-bold'> Friedrich Nietzsche  </span></h6>"
            customHeader
          >
          </Widget>
        </div>
      </b-col>
    </b-row>
  </div>
</template>

<script>
import Widget from "@/components/Widget/Widget";
import BigStat from "./components/BigStat/BigStat";
import mock from "./mock";
import { Chart } from "highcharts-vue";
import Card from "@/components/Card/Card";

export default {
  name: "Dashboard",
  components: {
    Widget,
    BigStat,
    highcharts: Chart,
    Card,
  },
  data() {
    return {
      mock,
    };
  },
  methods: {
    getRandomData() {
      const arr = [];

      for (let i = 0; i < 25; i += 1) {
        arr.push(Math.random().toFixed(1) * 10);
      }

      return arr;
    },
    getRevenueData() {
      const data = [];
      const seriesCount = 3;
      const accessories = ["SMX", "Direct", "Networks"];

      for (let i = 0; i < seriesCount; i += 1) {
        data.push({
          label: accessories[i],
          data: Math.floor(Math.random() * 100) + 1,
        });
      }

      return data;
    },
  },
  computed: {
    donut() {
      let revenueData = this.getRevenueData();
      let { danger, info, primary } = this.appConfig.colors;
      let series = [
        {
          name: "Revenue",
          data: revenueData.map((s) => {
            return {
              name: s.label,
              y: s.data,
            };
          }),
        },
      ];
      return {
        chart: {
          type: "pie",
          height: 120,
        },
        credits: {
          enabled: false,
        },
        title: false,
        plotOptions: {
          pie: {
            dataLabels: {
              enabled: false,
            },
            borderColor: null,
            showInLegend: true,
            innerSize: 60,
            size: 100,
            states: {
              hover: {
                halo: {
                  size: 1,
                },
              },
            },
          },
        },
        colors: [danger, info, primary],
        legend: {
          align: "right",
          verticalAlign: "middle",
          layout: "vertical",
          itemStyle: {
            color: "#495057",
            fontWeight: 100,
            fontFamily: "Montserrat",
          },
          itemMarginBottom: 5,
          symbolRadius: 0,
        },
        exporting: {
          enabled: false,
        },
        series,
      };
    },
  },
};
</script>

<style src="./Dashboard.scss" lang="scss" />
