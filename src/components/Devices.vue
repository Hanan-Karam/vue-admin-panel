<template>
    <div class="devices-container">
        <h2>Users by device</h2>
        <w-progress
            class="ma1"
            circle
            color="info"
            v-model="progress"
            size="10em">
            <strong>{{ progress }}%</strong>
        </w-progress>
        <div class="types">
            <span class="desktop"><i class="fa fa-circle" aria-hidden="true"></i>Desktop</span>
            <span class="mobile"><i class="fa fa-circle" aria-hidden="true"></i>Mobile</span>
        </div>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                progress:70,
            }
        }
    }
</script>
<style>
    .devices-container{
        background-color: white;
        padding:20px 35px;
        width:100%;
        border-radius: 10px;
        text-align: center;
    }
    h2{
        font-size: 16px;
        text-align: left;
        margin-bottom: 30px;
    }
    .types{
        margin-top:20px;
        display: flex;
        justify-content: space-between;
    }
    .types i{
        font-size: 10px !important;
        display: inline-block;
        margin-right: 5px;
    }
    span{
        font-size: 10px;
    }
    .desktop i{
        color:var(--light-blue)
    }
    .mobile i{
        color:#e5e5e5
    }
</style>