<template>
  <div>
    <b-card no-body class="skills-card">
      <b-nav pills card-header slot="header" v-b-scrollspy:nav-scroller="40">
        <b-nav-item href="#skills" @click="scrollIntoView">Skills</b-nav-item>
        <b-nav-item href="#education" @click="scrollIntoView"
          >Education</b-nav-item
        >
        <b-nav-item href="#experience" @click="scrollIntoView"
          >Experience</b-nav-item
        >
      </b-nav>

      <b-card-body id="nav-scroller" ref="content" class="skills-body">
        <div id="skills" class="pb-4">
          <b-row class="text-center">
            <b-col md="6" sm="12">
              <h5>Back-end</h5>
              <a href="https://www.php.net/" target="_blank" title="PHP">
                <img src="../../../public/php.svg" class="logo-tech" />
              </a>
            </b-col>
            <b-col md="6" sm="12">
              <h5>Front-end</h5>
              <a href="https://vuejs.org/" target="_blank" title="VueJs">
                <img src="../../../public/vue.svg" class="logo-tech vue" />
              </a>
            </b-col>
          </b-row>
          <b-row class="text-center">
            <b-col md="6" sm="12">
              <h5>DataBase</h5>
              <a href="https://www.mysql.com/" target="_blank" title="Mysql">
                <img src="../../../public/mysql.svg" class="logo-tech" />
              </a>
            </b-col>
            <b-col md="6" sm="12">
              <h5>Other</h5>
              <p>PHP</p>
            </b-col>
          </b-row>
        </div>

        <div id="education" class="pb-4">
          <h4>Education</h4>
          <b-list-group>
            <b-list-group-item href="#" class="flex-column align-items-start">
              <div class="d-flex w-100 justify-content-between">
                <h5 class="mb-1">bachelor in systems engineering</h5>
                <small class="text-muted">2016 - 2018</small>
              </div>

              <p class="mb-1">Unidades tecnologicas de santander</p>

              <small class="text-muted"></small>
            </b-list-group-item>

            <b-list-group-item href="#" class="flex-column align-items-start">
              <div class="d-flex w-100 justify-content-between">
                <h5 class="mb-1">Certificate IV in Information Technology</h5>
                <small class="text-muted">2019 - 2020</small>
              </div>

              <p class="mb-1">
               Academies Australasia Polytechnic
              </p>

              <small class="text-muted">Information Technology</small>
            </b-list-group-item>
          </b-list-group>
        </div>

        <div id="experience">
          <h4>Experience</h4>
          <b-list-group>
            <b-list-group-item href="#" class="flex-column align-items-start">
              <div class="d-flex w-100 justify-content-between">
                <h5 class="mb-1">Full Stack Developer</h5>
                <small class="text-muted">2021</small>
              </div>

              <p class="mb-1">Unidades tecnologicas de santander</p>

              <small class="text-muted">Donec id elit non mi porta.</small>
            </b-list-group-item>

            <b-list-group-item href="#" class="flex-column align-items-start">
              <div class="d-flex w-100 justify-content-between">
                <h5 class="mb-1">Disabled List group item</h5>
                <small class="text-muted">3 days ago</small>
              </div>

              <p class="mb-1">
                Donec id elit non mi porta gravida at eget metus. Maecenas sed
                diam eget risus varius blandit.
              </p>

              <small class="text-muted">Donec id elit non mi porta.</small>
            </b-list-group-item>
          </b-list-group>
        </div>
      </b-card-body>
    </b-card>
  </div>
</template>

<script>
export default {
  methods: {
    // Convenience method to scroll a heading into view.
    // Not required for scrollspy to work
    scrollIntoView(event) {
      event.preventDefault();
      const href = event.target.getAttribute("href");
      const el = href ? document.querySelector(href) : null;
      if (el) {
        console.log(el.offsetTop);
        this.$refs.content.scrollTop = el.offsetTop;
      }
    },
  },
  data() {
    return {
      text: `
          Quis magna Lorem anim amet ipsum do mollit sit cillum voluptate ex nulla
          tempor. Laborum consequat non elit enim exercitation cillum aliqua
          consequat id aliqua. Esse ex consectetur mollit voluptate est in duis
          laboris ad sit ipsum anim Lorem. Incididunt veniam velit elit elit veniam
          Lorem aliqua quis ullamco deserunt sit enim elit aliqua esse irure. Laborum
          nisi sit est tempor laborum mollit labore officia laborum excepteur
          commodo non commodo dolor excepteur commodo. Ipsum fugiat ex est consectetur
          ipsum commodo tempor sunt in proident.
        `,
    };
  },
  mounted() {
    // this.$refs.content.scrollTop = el.offsetTop;
  },
};
</script>

<style src="./Skills.scss" lang="scss" />