<template>
  <div class="dashboard-page">
    <b-row>
      <b-col sm="6" xs="12" class="pb-lg">
        <Widget class="h-100 mb-0">
          <Card />
        </Widget>
      </b-col>
      <b-col sm="6" xs="12" class="pb-lg">
        <b-row>
          <b-col sm="12" xs="12" class="pb-2">
            <Widget class="mb-3">
              <div class="effect egeon">
                <div class="buttons">
                  <a href="https://github.com/hleomojica/" target="_blank" class="github" title="Github"
                    ><i class="fa fa-github" aria-hidden="true"></i
                  ></a>
                  <a href="https://linkedin.com/in/hleomojica" class="in" target="_blank" title="Join us on Linked In"
                    ><i class="fa fa-linkedin" aria-hidden="true"></i
                  ></a>
                  <a href="#" class="fb" title="Join us on Facebook"
                    ><i class="fa fa-facebook" aria-hidden="true"></i
                  ></a>
                  
                  <a href="#" class="tw" title="Join us on Twitter"
                    ><i class="fa fa-twitter" aria-hidden="true"></i
                  ></a>
                  <a href="#" class="g-plus" title="Join us on Google+"
                    ><i class="fa fa-google-plus" aria-hidden="true"></i
                  ></a>
                  
                  
                </div>
              </div>
            </Widget>
          </b-col>
          <b-col sm="12" xs="12" class="">
            <Widget class="h-100 mb-3">
              <h2 style="text-align: center">Site in construction</h2>
            </Widget>
          </b-col>
        </b-row>
      </b-col>
    </b-row>
    <b-row class="h-100">
      <b-col xs="12" class="pb-sm h-100">
        <Widget title="" class="mb-4 h-100" customHeader>
          <div id="avatar">
            <img src="../../assets/dev2.svg" alt="" />
          </div>
        </Widget>
      </b-col>
    </b-row>
    <b-row>
      <b-col xs="12">
        <div class="h-100 pb-xlg">
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
