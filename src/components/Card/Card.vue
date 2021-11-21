<template>
  <div>
    <b-card class="overflow-hidden text-center" >
      <b-row no-gutters>
        <b-col md="4" sm="12">
          <b-card-img
            src="../../assets/me2.jpeg"
            alt="Image"
            class="img-card img-fluid"
          ></b-card-img>
        </b-col>
        <b-col md="8" sm="12">
          <b-card-body>
            <b-card-title> <h3>HENRRY MOJICA</h3> </b-card-title>
            <b-card-sub-title class="mb-2">
              <h5>Full Stack Software developer</h5>
            </b-card-sub-title>
            <b-card-text>
              <a href="https://vuejs.org/" target="_blank" title="VueJs">
                <img src="../../../public/vue.svg" class="logo-tech vue" />
              </a>
              <a href="https://www.mysql.com/" target="_blank" title="Mysql">
                <img src="../../../public/mysql.svg" class="logo-tech" />
              </a>
              <a href="https://www.php.net/" target="_blank" title="PHP">
                <img src="../../../public/php.svg" class="logo-tech" />
              </a>
            </b-card-text>
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
