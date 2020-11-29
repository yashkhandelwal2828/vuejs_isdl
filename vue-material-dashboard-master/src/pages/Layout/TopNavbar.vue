<template>
<!-- <mdb-container> -->

<b-container fluid>

    <b-navbar toggleable="lg" type="dark">
        <b-navbar-brand href="#" style="color:#495057!important; font-size:18px;">
            <h4>{{ $route.name }}</h4>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>

            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
                <b-nav-form class="icons">
                    <b-form-input list="my-list-id" size="sm" class="mr-sm-2" placeholder="Search">
                    </b-form-input>
                    <datalist id="my-list-id">
                        <option :key="employee" v-for="employee in employees">{{ employee }}</option>
                    </datalist>
                </b-nav-form>
                <b-nav-item class="icons" href="#/dashboard">
                    <!-- <span class="material-icons" animation="fade" style="color:#495057!important; font-size:20px;">
                        dashboard
                    </span> -->
                    <b-icon variant="dark" icon="columns-gap"></b-icon>
                </b-nav-item>
                <!-- <b-nav-item class="icons" href="#/notifications">
                        <span class="notification-number">
                            5
                        </span>
                    <b-icon variant="dark" icon="bell-fill"></b-icon>


                </b-nav-item>
                    <b-dropdown-item href="#">Action</b-dropdown-item>
                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
              </b-dropdown> -->

                <b-nav-item class="px-0 py-0 icons"  href="#/notifications">
                        <!-- <template #button-content  href="#/notifications"> -->
                    <b-dropdown size="md"  variant="link" toggle-class="text-decoration-none" no-caret>
                        <template #button-content href="#/notifications"> 
                                <b-icon href="#/notifications" variant="dark" icon="bell-fill"></b-icon>
                        </template>
                            <b-dropdown-item href="#">Action</b-dropdown-item>
                            <b-dropdown-item href="#">Another action</b-dropdown-item>
                            <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                    </b-dropdown>
                </b-nav-item>
                
<!--              
                    </b-dropdown> -->
                <b-nav-item class="icons" href="#/user">

                    <b-icon variant="dark" icon="person-fill"></b-icon>

                    <!-- <span class="material-icons" list="my-list-id" style="color:#495057!important; font-size:20px;">
                        person
                    </span> -->
                    <datalist id="my-list-id">
                        <option :key="employee" v-for="employee in employees">{{ employee }}</option>
                    </datalist>
                </b-nav-item>
            </b-navbar-nav>
        </b-collapse>
    </b-navbar>

</b-container>
</template>

<script>
export default {
    data() {
        return {
            // selectedEmployee: null,
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
        },
        iconClick(){
            
        }
    },
    name: 'TopNavbar',
    components: {

    }

};
</script>

<style lang="css">
/* .dashboard__icon {
    background-color: "#000" !important;
    color: "black" !important;
} */

/* .icon {
    color: #495057;
}*/
.navbar {
    /* padding: 0.625 rem;
    height: 3.125rem; */
    min-height: auto;
    padding-left: 15px;
    padding-right: 15px;
}

.notification-number {
       position: absolute;
    top: 21px;
    border: 1px solid #fff;
    right: 78px;
    font-size: 10px !important;
    background: #f44336;
    color: #fff !important;
    z-index: 1;
    min-width: 10px;
    padding: 0 5px;
    /* height: 15px; */
    border-radius: 50px;
    text-align: center;
    line-height: 15px;
    display: block;
}

.icons {
    padding: 9px;
    border-radius: 3px
}

/*
.h3 {
    color: #495057
} */
</style>
_icon
