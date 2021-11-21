<template>
  <b-navbar toggleable="lg" class="header d-print-none app-header">
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-nav class="d-md-down-none">
      <a href="" class="headertex"> MOJIDEV </a>
    </b-nav>

    <a class="navbarBrand d-md-none">
      <a href="/" class="headertex"> M D</a>
    </a>

    <b-collapse id="nav-collapse" is-nav>
      <b-nav class="mx-auto">
        <b-nav-item>
          <a href="/" class="menu"> About me</a>
        </b-nav-item>
        <b-navbar-nav class="headertex mr-4">
          <a href="/" class="menu"> Proyects</a>
        </b-navbar-nav>
        <b-navbar-nav class="headertex">
          <a href="/" class="menu"> Extra</a>
        </b-navbar-nav>
      </b-nav>
    </b-collapse>

    <b-nav class="ml-auto">
      <b-navbar-nav>
        <div class="effect egeon">
          <div class="buttons w-100">
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
      </b-navbar-nav>
      <b-nav-item-dropdown
        id="v-step-2"
        class="settingsDropdown d-sm-down-none"
        no-caret
        right
      >
        <template slot="button-content">
          <i class="fi flaticon-settings-10 px-2" />
        </template>
        <b-dropdown-item
          ><i class="fi flaticon-person px-3 mr-3" /> Log in</b-dropdown-item
        >
        <b-dropdown-divider />
        <b-dropdown-item
          ><i
            class="fi flaticon-calendar-9 px-3 mr-3"
          />Calendar</b-dropdown-item
        >
        <b-dropdown-item
          ><i class="fi flaticon-email px-3 mr-3" /> Inbox &nbsp;&nbsp;<b-badge
            variant="inverse"
            pill
            class="animate__animated animate__bounceIn"
            style="padding: 6px 9px"
            >9</b-badge
          >
        </b-dropdown-item>
        <b-dropdown-divider />
        <b-dropdown-item-button @click="logout">
          <i class="fi flaticon-power-1 px-3 mr-3" /> OFF
        </b-dropdown-item-button>
      </b-nav-item-dropdown>
    </b-nav>
  </b-navbar>
</template>

<script>
import { mapState, mapActions } from "vuex";
import Notifications from "@/components/Notifications/Notifications";

export default {
  name: "Header",
  components: { Notifications },
  computed: {
    ...mapState("layout", ["sidebarClose", "sidebarStatic"]),
  },
  methods: {
    ...mapActions("layout", [
      "toggleSidebar",
      "switchSidebar",
      "changeSidebarActive",
    ]),
    switchSidebarMethod() {
      if (!this.sidebarClose) {
        this.switchSidebar(true);
        this.changeSidebarActive(null);
      } else {
        this.switchSidebar(false);
        const paths = this.$route.fullPath.split("/");
        paths.pop();
        this.changeSidebarActive(paths.join("/"));
      }
    },
    toggleSidebarMethod() {
      if (this.sidebarStatic) {
        this.toggleSidebar();
        this.changeSidebarActive(null);
      } else {
        this.toggleSidebar();
        const paths = this.$route.fullPath.split("/");
        paths.pop();
        this.changeSidebarActive(paths.join("/"));
      }
    },
    logout() {
      // window.localStorage.setItem('authenticated', false);
      // this.$router.push('/login');
    },
  },
};
</script>

<style src="./Header.scss" lang="scss"></style>
