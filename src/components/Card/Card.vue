<template>
  <div>
    <b-card class="overflow-hidden text-center">
      <b-row no-gutters>
        <b-col
          md="2"
          lg="4"
          sm="12"
          class="d-flex align-items-center justify-content-center"
        >
          <div class="spin circle">
            <b-card-img
              src="../../assets/me2.jpeg"
              alt="Image"
              class="img-card img-fluid"
            ></b-card-img>
          </div>
        </b-col>
        <b-col md="10" lg="8" sm="12">
          <b-card-body>
            <b-card-title> <h3>HENRRY MOJICA</h3> </b-card-title>
            <b-card-sub-title class="mb-2">
              <h5>Full Stack Software developer</h5>
            </b-card-sub-title>
            <b-card-text class="text-justify">
              Curious and passionate about learning new stuff. 2+ years of
              experience building web applications and Enterprise solutions for
              Med/big companies ERP, POS. Knowledge using DevTools stacks and
              teamwork solutions such as JIRA, Confluence, and GIT
            </b-card-text>
            <!-- <b-card-text>
              <a href="https://vuejs.org/" target="_blank" title="VueJs">
                <img src="../../../public/vue.svg" class="logo-tech vue" />
              </a>
              <a href="https://www.mysql.com/" target="_blank" title="Mysql">
                <img src="../../../public/mysql.svg" class="logo-tech" />
              </a>
              <a href="https://www.php.net/" target="_blank" title="PHP">
                <img src="../../../public/php.svg" class="logo-tech" />
              </a>
            </b-card-text> -->
          </b-card-body>
        </b-col>
      </b-row>
    </b-card>
  </div>
</template>

<script>
import Loader from "../Loader/Loader";

export default {
  name: "Card",
  props: {},
  components: { Loader },
  computed: {
    randomId() {
      return Math.floor(Math.random() * 100);
    },
  },
  mounted() {},
  methods: {},
};
</script>

<style src="./Card.scss" lang="scss"  scoped/>
