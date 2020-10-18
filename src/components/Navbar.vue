<template>
<div>
<nav>
    <ul>
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/about">About</router-link></li>
        <li><router-link to="/contact">Contact</router-link></li>

    </ul>
</nav>
<div>
    <ul>
        <li v-for="(id,index) in userIds" :key="index">
            <router-link :to="{name:'Profile', params:{getid:id}}" >Profile {{id}}</router-link>
        </li>
    </ul>
    <button @click="contactPage">Contact</button>
    <button @click="aboutPage">About</button>
</div>
</div>
</template>
<script>
export default {
    name:'Navbar',
    data(){
        return {
            userIds:['1','2','3','4',]

        }
    },
    methods:{
        contactPage(){
            this.$router.push({name:'Contact'})
        },
        aboutPage(){
            this.$router.push({name:'About'})
        }
    }
    
}
</script>
<style>
nav {
    text-align: center;
}
nav ul{
    padding:0px;
}
nav li{
    display: inline-block;
    list-style-type: block;
    margin: 0px;
    padding:10px;
}

</style>