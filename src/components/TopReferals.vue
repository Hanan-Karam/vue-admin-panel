<template>
    <div class="referals-container">
        <div class="heading">
            <h3>Top Referals</h3>
            <h4>View All</h4>
        </div>
        <div class="referal" v-for="referal in referals" :key="referal.name">
            <i :class="referal.icon" :id="referal.color"></i>
            <p>{{referal.name}}</p>
            <p>{{referal.value}}</p>
        </div>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                referals:[
                    {name:"FaceBook", icon:"fa fa-facebook", value: 234, color:"blue"},
                    {name:"Twitter", icon:"fa fa-twitter", value: 234, color:"blue"},
                    {name:"Google", icon:"fa fa-google-plus", value: 234, color:"orange"},
                    {name:"YouTube", icon:"fa fa-youtube-play", value: 234, color:"red"},
                ]
            }
        }
    }
</script>
<style>
    .referals-container{
        background-color: white;
        width:30%;
        height: 90%;
        margin: auto;
        padding:20px;
        border-radius: 10px;
    }
    .referal, .heading {
        display: grid;
        grid-template-columns: 1fr 2fr 1fr;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 15px;
    }
    .heading{
        grid-template-columns: 2fr  1fr;
        margin-bottom: 25px;
    }
    .heading h3{
        font-size: 14px;
    }
     .heading h4{
        font-size: 12px;
        color:gray;
    }
    .referal #red, #orange, #blue{
        font-size:18px !important;
        width:30px;
        height:30px;
        border-radius: 50%;
    }
    #red{
        background-color: #f2aeae;
        color:#db2b2b;
    }
    p{
        color:#333;
    }

</style>