<template>
  <div>
    <div class="row d-flex justify-content-center">
      <div class="col-12 mt-5">
        <h3 class="text-center">Select an Action</h3>
      </div>
      <div class="col-12 col-sm-8 col-md-6">
        <b-list-group v-for='(item ,index) in homeListItems' :key="index">
          <router-link :to='item.url' :tag="item.tag" :target="item.target" class="list-group-item list-group-item-action">
            {{ item.description }}
          </router-link>
        </b-list-group>
        <b-list-group button>
          <b-list-group-item button>Download patient data csv file</b-list-group-item>
        </b-list-group>
        <div class="text-right mt-5">
            <b-button size="sm" variant="outline-secondary">Logout</b-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      homeListItems: [
        {
          description: 'Add a new patient',
          url: {
            name: 'PatinetCreate'
          },
          target: '_self',
          tag: 'button'
        },
        {
          description: 'Capture existing patient data',
          url: {
            name: 'PatientFind'
          },
          target: '_self',
          tag: 'button'
        }
      ]
    }
  },
  components: {
  }
}
</script>

<style lang="scss" scoped>
    @import '../assets/styles/variableOverride.scss';

    .list-group-item{
    margin-top: 1rem;
    border-width: 0.063rem;
    box-shadow: 0.063rem 0.125rem 0.188rem #cccccc9e;
    outline: none !important;
    text-align: center;
  }

  .list-group-item + .list-group-item.active{
        margin-top: 1rem;
  }
  .list-group-item-action:hover, .list-group-item-action:focus{
    background-color: $blue;
    color: $white;
  }
</style>
