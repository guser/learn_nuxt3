<template>
    <div id="container">
        <slot />
    </div>  
</template>

<style>
.container {
    display: auto 0;

}

form {
    width: 480px;

    display: flex;
    flex-direction: column;
}

 form input {

    padding: 8px;
    margin: 4px;
}
</style>
