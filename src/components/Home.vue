<template>
    <div>
        <h1>{{ data }}</h1>
        <h2>{{ msg }}</h2>
    </div>
</template>
<script>
export default {
    name:'Home',
    props:{
        data:String,
        msg:String,
    }
};
</script>