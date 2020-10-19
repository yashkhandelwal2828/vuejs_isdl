<template>

 




    <!-- <mdb-container> -->
        <mdb-navbar>
          <mdb-navbar-brand class="heading">
            <h3>{{ $route.name }}</h3>
          </mdb-navbar-brand>
          <mdb-navbar-toggler>
            <mdb-navbar-nav right>
              <form>
                <mdb-input type="text" class="text-white" placeholder="Search" aria-label="Search" label navInput waves waves-fixed/>
              </form>
              <mdb-nav-item v-mdb-waves  href="#/"><mdb-icon v-mdb-waves class="icon" icon="th-large" size="lg" /></mdb-nav-item>
                <mdb-nav-item v-mdb-waves  href="#/notifications"><mdb-icon class="icon"  icon="bell" size="lg" /></mdb-nav-item>
               <mdb-nav-item v-mdb-waves  href="#/user"><mdb-icon class="icon" icon="user" size="lg" /></mdb-nav-item>
            </mdb-navbar-nav>
          </mdb-navbar-toggler>
        </mdb-navbar>
    <!-- </mdb-container> -->




  <!-- <mdb-toolbar md-elevation="0" class="md-transparent">
    <div class="md-toolbar-row">
      <div class="md-toolbar-section-start">
        <h3 class="md-title">{{ $route.name }}</h3>
      </div>
      <div class="md-toolbar-section-end">
        <md-button
          class="md-just-icon md-simple md-toolbar-toggle"
          :class="{ toggled: $sidebar.showSidebar }"
          @click="toggleSidebar"
        >
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </md-button>

        <div class="md-collapse">
          <div class="md-autocomplete">
            <md-autocomplete
              class="search"
              v-model="selectedEmployee"
              :md-options="employees"
            >
              <label>Search...</label>
            </md-autocomplete>
          </div>
          <md-list>
            <md-list-item href="#/">
              <i class="material-icons">dashboard</i>
              <p class="hidden-lg hidden-md">Dashboard</p>
            </md-list-item>

            <li class="md-list-item">
              <a
                href="#/notifications"
                class="md-list-item-router md-list-item-container md-button-clean dropdown"
              >
                <div class="md-list-item-content">
                  <drop-down>
                    <md-button
                      slot="title"
                      class="md-button md-just-icon md-simple"
                      data-toggle="dropdown"
                    >
                      <b-icon-bell-fill font-scale='0.9'>notifications</b-icon-bell-fill>   
                      <span class="notification">5</span>
                      <p class="hidden-lg hidden-md">Notifications</p>
                    </md-button>
                    <ul class="dropdown-menu dropdown-menu-right">
                      <li><a href="#">Mike John responded to your email</a></li>
                      <li><a href="#">You have 5 new tasks</a></li>
                      <li><a href="#">You're now friend with Andrew</a></li>
                      <li><a href="#">Another Notification</a></li>
                      <li><a href="#">Another One</a></li>
                    </ul>
                  </drop-down>
                </div>
              </a>
            </li>

            <md-list-item href="#/user">
           <b-icon-person-fill font-scale='2'>person</b-icon-person-fill> 
              <p class="hidden-lg hidden-md">Profile</p>
            </md-list-item>
          </md-list>
        </div>
      </div>
    </div>
  </mdb-toolbar> -->
</template>

<script>

 import { mdbNavbar, mdbNavbarBrand,   mdbNavbarToggler, mdbIcon, mdbNavbarNav, mdbNavItem, mdbDropdown, mdbDropdownMenu,mdbWaves, mdbDropdownToggle, mdbInput, mdbDropdownItem } from 'mdbvue';
  
export default {
  data() {
    return {
      selectedEmployee: null,
      employees: [
        "Jim Halpert",
        "Dwight Schrute",
        "Michael Scott",
        "Pam Beesly",
        "Angela Martin",
        "Kelly Kapoor",
        "Ryan Howard",
        "Kevin Malone"
      ]
    };
  },
  methods: {
    toggleSidebar() {
      this.$sidebar.displaySidebar(!this.$sidebar.showSidebar);
    }
  },
    name: 'TopNavbar',
    components: {
      mdbNavbar,
      mdbNavbarBrand,
      mdbNavbarToggler,      
       mdbIcon,
      mdbNavbarNav,
      mdbInput,
      mdbNavItem
     

    },
    directives:{
      mdbWaves
    }
};
</script>

<style lang="css">
  .icon {
    color: #495057;
  }
  .h3{
    color: #495057
  }
</style>
