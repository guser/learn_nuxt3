<template>
    <p>
        Register
    </p>

    <div>
        <form>
            <input v-model="first_name" placeholder="First Name" />
            <input v-model="email" placeholder="Email" />
            <input v-model="mobile" placeholder="Mobile Number" />
            <input v-model="password" type="password" placeholder="Password" />

            <br/>
            <input v-model="city" placeholder="City" />
            <input v-model="country" placeholder="Country" />
            
            <input type="submit" value="Submit" @click.prevent="createUser"/>
        </form>
    </div>

</template>

<script setup >

    const first_name = ref('');
    const email = ref('');
    const mobile = ref('');
    const password = ref('');
    const city = ref('');
    const country = ref('');

    async function createUser() {

        const URL = "https://3000-guser-base-x6edhj2hepj.ws-us79.gitpod.io/users";
        
        const form = {
            first_name: first_name.value,
            email: email.value,
            mobile: mobile.value,
            password: password.value, 
            city: city.value, 
            country: country.value,
        };

        const options = {
            method: "POST",
            mode: 'no-cors',
            body: JSON.stringify(form),

        };

        const response = await fetch(URL, options );
    }
</script>