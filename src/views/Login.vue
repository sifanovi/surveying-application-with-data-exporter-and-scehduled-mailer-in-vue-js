<template>
  <div>
    <h2 class="text-primary text-center">COVID-19 ASSESSMENT PORTAL</h2>
    <div class="row justify-content-center d-flex">
      <div class="col-12 col-md-6">
        <b-card class="mt-3 login-card">
          <b-form>
            <b-row class="my-1 mb-3" v-for="(field, index) in loginFields" :key="index">
              <b-col sm="3">
                <label :for="`type-${ field.label }`">
                  {{ field.label }}
                </label>
              </b-col>
              <b-col sm="9">
                <b-form-input :id="`type-${field.type}`" :type="field.type" v-model="field.value" :placeholder="field.placeholder"></b-form-input>
              </b-col>
            </b-row>
            <div class="text-right">
              <b-button type="button" variant="primary">Login</b-button>
            </div>
          </b-form>
        </b-card>
      </div>
    </div>
    <Disclaimer />
  </div>
</template>
<script>
import disclaimer from '../components/Disclaimer'

export default {
  name: 'Login',
  data () {
    return {
      loginFields: [
        { label: 'Username:', type: 'text', placeholder: 'e.g. johndoe', value: '' },
        { label: 'Password:', type: 'password', placeholder: '*****', value: '' }
      ]
    }
  },
  components: {
    Disclaimer: disclaimer
  }
}
</script>
<style lang="scss" scoped>
  .login-card{
    box-shadow: 1px 2px 5px 2px #b7b7b766;
    border: 0px;
    border-radius: 0px;
  }
</style>
