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
      <Widget class="w-100">
        <Skills />
      </Widget>
    </b-row>
    <!-- Projects section -->
    <b-row>
      <b-col md="12">
        <Widget
          title="<h5>Recent  <span class='fw-semi-bold'>Projects</span></h5>"
          customHeader
        >
          
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
    
    
  </div>
</template>

<script>
import Widget from "@/components/Widget/Widget";
import BigStat from "./components/BigStat/BigStat";
import mock from "./mock";
import { Chart } from "highcharts-vue";
import Card from "@/components/Card/Card";
import Skills from "@/components/Skills/Skills";

export default {
  name: "Dashboard",
  components: {
    Widget,
    BigStat,
    highcharts: Chart,
    Card,
    Skills,
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
