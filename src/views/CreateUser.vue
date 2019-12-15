<template>
    <div>
        <b-form id="reg" @submit="onSubmit">
            <b-form-group
            id="input-group-1"
            class="form-group"
            label = 'Firstname:'
            label-cols-sm="4"
            label-cols-lg="3"
            >
            <b-form-input
                id="input-1"
                v-model="form.firstname"
                type="text"
                required
                placeholder="Enter Firstname"
                ></b-form-input>   
            </b-form-group>
            <b-form-group
            id="input-group-2"
            class="form-group"
            label = 'Lastname:'
            label-cols-sm="4"
            label-cols-lg="3"
            >
            <b-form-input
                id="input-2"
                v-model="form.lastname"
                type="text"
                required
                placeholder="Enter Lastname"
                ></b-form-input>   
            </b-form-group>
            <b-form-group
            id="input-group-3"
            class="form-group"
            label='Email:'
            label-cols-sm="4"
            label-cols-lg="3"
            >
            <b-form-input
                id="input-3"
                v-model="form.email"
                type="text"
                required
                placeholder="Enter Email Address"
                ></b-form-input>   
            </b-form-group>
            <b-form-group
            id="input-group-4"
            class="form-group"
            label='Role:'
            label-cols-sm="4"
            label-cols-lg="3"
            >
            <b-form-select
                id="input-2"
                v-model="form.selectRole"
                :options="roles"
                >
                </b-form-select>   
            </b-form-group>
            <b-button type="submit" variant="primary">Submit</b-button>
        </b-form>
    </div>
</template>

<script>
export default {
    name: 'CreateUserForm',
    data(){
        return{
            form:{
                firstname: '',
                lastname: '',
                email: '', 
            },
            roles: [{value: null, text: 'Select one'},
            {value: 1, text: 'QA'},
            {value: 2, text: 'Developer'},
            {value: 3, text: 'User Tester'},
            {value: 4, text: 'Project manager'}]
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
#reg{
    display: flex;
    flex-direction: column;
}
.form-group{
padding-right: 10%;
}
</style>