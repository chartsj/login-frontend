<template>

    <form class="card-login">
        <h1 class="login-title">Login</h1>
        <div>
            <label>Email</label><br>
            <input type="text"><br>
        </div>
        <div>
            <label>Password</label><br>
            <input type="text"><br>
        </div>
        
        <button class="login-button">Sign In</button>
    </form>
</template>
<style scoped>

input{
    width:100%
}
label{
    font:Inter;
    color:black;
    font-weight: 400;
  
}
.login-button{
    width:100%;
    background: #2563eb;
    padding: 0.9rem 1.2rem;
    border:none;
    border-radius: 0.75rem;
    color:white;
    font-weight: 600;
    font-size: 1rem;
    cursor:pointer;
    margin-top: 1rem;
}

.login-title{
    text-align: center;
    
}

.card-login{
    background-color: white ;
    padding: 1.5rem;
    display:flex;
    flex-direction: column;
    gap:1rem;
    width:20rem;
    border-radius: 12px;

}
</style>
