<script setup>
import { ref } from 'vue';
    async function handleSubmit(event){
        event.preventDefault()
        console.log(JSON.stringify({"username":username.value, "password":password.value}))        
        // const res = await fetch('http://127.0.0.1:8000/api/login',
        // {
        //     method: "POST",
        //     headers: {
        //     "Content-Type": "application/json",
        //     },
        //     body: JSON.stringify({"username":username.value, "password":password.value})
        // })
        // const data = await res.json()

    }             
    
    let username = ref("")
    let password = ref("")
    
</script>
<template>
 <div class="row col-6">      

        <h1 class="my-5">Login</h1>
        <form @submit="handleSubmit">
            
            <div class="form-outline mb-4">
                <input type="text" class="form-control" id="username" v-model="username">

                <label class="form-label" for="username">Email address</label>
            </div>

            
            <div class="form-outline mb-4">
                <input type="password" id="password" v-model="password" class="form-control"/>
                <label class="form-label" for="password">Password</label>
            </div>


            
            <button type="submit" class="btn btn-primary btn-block mb-4">Sign in</button>

            
            <div class="text-center">
                <p>Not a member? <a href="">Register</a></p>
            </div>
        </form>
    </div>
</template>

<style>
.products {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin: 50px;
}
</style>