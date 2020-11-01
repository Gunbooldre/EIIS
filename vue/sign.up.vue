<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<template>
    <form class = "mt- 5">
        <div class = "form-group">
            <label for = "email" >Your email</label>
            <input type = "email" class = "form-control" id = "email" placeholder = "Enter a email:" required >
        </div>
        <div class = "form-group">
            <label for = "password" >Enter your password </label>
            <input type = "password" class = "form-control" id = "password" placeholder = "Enter a password:" required >
        </div>
        <div class = "form-group">
            <label for = "password2" >Please repeat your password</label>
            <input type = "password" class = "form-control" id = "password2" placeholder = "Enter a password:" required >
        </div>
        <div class  = "alert alert-danger "  role = "alert" v-if = "error">
            <strong>Ops...</strong> password is not same
        </div>
        <button type = "submit" class = "btn btn-primary" >Registration</button>    
    </form>
</template>

    <script>
        export default{
            name:'sign-up',
            data(){
                return{
                    user:{
                        email:'',
                        password:'',
                        confirmation:''
                    }
                    error:false
                }
            }
        }
    </script>