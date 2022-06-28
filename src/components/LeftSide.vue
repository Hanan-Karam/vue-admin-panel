<template>
    <div class="left-container">
        <div class="logo">
            <i class="fa fa-bolt" aria-hidden="true" id="logo-icon"></i>
            <span class="name">ZHard.com</span>
        </div>
        <div class="menu">
            <ul>
                <li v-for="item in items">
                    <i :class="item.icon" aria-hidden="true"></i>
                    <span>{{item.title}}</span>
                </li>

                <hr>

                <li>
                    <i class="fa fa-cog" aria-hidden="true"></i>
                    <span>Settings</span>
                </li>
                <li>
                    <i class="fa fa-sign-out" aria-hidden="true"></i>
                    <span>Logout</span>
                </li>
            </ul>
        </div>
        <div class="draft">
            <i class="fa fa-file " aria-hidden="true"></i>
            <h4>New Draft</h4>
            <p>Do you want to make new draft to write something?</p>
            <button>Create File</button>
        </div>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                items:[
                    {title:"Dashboard", icon:"fa fa-th-large"},
                    {title:"Blog Post", icon:"fa fa-file-text"},
                    {title:"Messages", icon:"fa fa-envelope"},
                    {title:"Statistics", icon:"fa fa-bar-chart"},
                ]
            }
        }
    }
</script>
<style>
.left-container{
     background-color: white;
     padding: 25px 20px;
     height: 100%;
     border-top-left-radius: 20px;
     border-bottom-left-radius: 20px;
    }
    .logo, li, .draft{
        display: flex;
        gap: 10px;
        justify-content: left;
        align-items: center;
    }
    #logo-icon{
        background: var(--light-blue);
        display: inline-block;
        width: 35px;
        height: 35px;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        border-radius: 50%;
    }
    .name{
        color:var(--light-blue);
        font-size: 16px;
        font-weight: 500;
    }
    ul{
        list-style: none;
        margin-top: 30px;
    }
    li{
        justify-content: left;
        padding:10px 10px;
        width: 130px;
        margin-top: 10px;
        color:var(--menue-text)
    }
    li span{
        display: inline-block;
        text-align: right;
        align-self: flex-start;
        font-weight: 500;
        font-size: 14px;
    }
    li span:hover{
        color:var(--light-blue)
    }
    i{
        font-size: 20px !important;
    }
    i:hover{
        color:var(--light-blue)
    }
    li:hover{
        background-color: #ecf0f9;
        border-radius: 7px;
        color:var(--light-blue)
    }
    .draft{
        flex-direction: column;
        font-size: 14px;
        margin-top: 30px;
        background: #ecf0f9;
        padding: 20px 10px;
        border-radius: 10px;
    }
    .draft i{
        color:var(--light-blue);
        font-size: 30px !important;
    }
    .draft p{
        color:#666;
        text-align: center;
        font-size: 12px;
    }
    .draft button{
        padding:10px 20px;
        font-size: 11px;
        border: none;
        background-color: white;
        border-radius: 7px;
        color:var(--light-blue)
    }
    hr{
        color:var(--menue-text);
        width:80%;
        margin: auto;
    }



</style>