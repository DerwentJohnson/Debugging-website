<template>
    <div id="cardholder">
      <b-card id="card" title="Login">
      <b-form id="form" @submit="onSubmit"  >
      <b-form-group
        id="input-group-1"
        label-cols-sm="4"
        label-cols-lg="3"
        label="Email address:"
        label-for="input-1"
      >
        <b-form-input
          id="input-1"
          v-model="form.email"
          type="email"
          required
          placeholder="Enter email"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2"
                    label="Password:"
                    label-cols-sm="4"
                    label-cols-lg="2"
                    label-for="input-2">
        <b-form-input
          type="password" id="text-password"
          v-model="form.password"
          placeholder="Password"
          aria-describedby="password-help-block"
        ></b-form-input>
      </b-form-group>
      <b-button type="submit" variant="primary">Submit</b-button>
    </b-form>
      </b-card>
    </div>
</template>

<script>

export default {
  components: {
    
  },
    data() {
      return {
        form: {
          email: '',
          password: ''
        },
        
      }
    },
    methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form))
      }
     
    }
  }
</script>

<style scoped>
#form{
  padding: 30px
}
#cardholder{
  display: flex;
  justify-content: center;
}
#card{
  width: 50%;
}

</style>