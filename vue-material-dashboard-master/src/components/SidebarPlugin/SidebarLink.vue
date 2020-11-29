<template>
<!--<li class="md-list-item">
    <router-link class="md-list-item-router md-list-item-container md-button-clean" @click="hideSidebar" v-bind="$attrs">
        <div class="md-list-item-content md-ripple">
            <slot>
                <b-icon>{{ link.icon }}</b-icon>
                <p>{{ link.name }}</p>
            </slot>
        </div>
    </router-link> -->
    <b-list-group-item>
     <b-link class="list" @click="hideSidebar" v-bind="$attrs">
        <div >
            <slot>
                <b-icon>{{ link.icon }}</b-icon>
                <p>{{ link.name }}</p>
            </slot>
        </div>
    </b-link>
   
</b-list-group-item>
</template>

<script>
export default {
    inject: {
        autoClose: {
            default: true
        }
    },
    props: {
        link: {
            type: [String, Object],
            default: () => {
                return {
                    name: "",
                    path: "",
                    icon: ""
                };
            }
        },
        tag: {
            type: String,
            default: "b-link"
        }
    },
    methods: {
        hideSidebar() {
            if (
                this.autoClose &&
                this.$sidebar &&
                this.$sidebar.showSidebar === true
            ) {
                this.$sidebar.displaySidebar(false);
            }
        }
    }
};
</script>

<style>
  .list-group-item{
      background-color:inherit !important;
      border:0px;
      margin-left:1.5625rem;
      margin-bottom:0.375rem;
  }
  .list-group-item p{
      color:white;
  }
  .list-group-item:last-child{
      margin-top:1.875rem;
  }
  ::v-deep .list {
    background-color: green;
  }
  .list:focus{
    background-color: green;
      
  }

</style>
