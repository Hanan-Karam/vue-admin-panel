<template>
    <div class="discussion">
        <div class="heading">
            <h3>Discussion</h3>
            <h4>View All</h4>
        </div>
        <div class="chat" v-for="chat in chats">
            <img :src="chat.src" alt="">
            <div>
                <p>{{chat.name}}</p>
                <p>{{chat.date}}</p>
            </div>
            <i class="fa fa-ellipsis-v" aria-hidden="true"></i>
        </div>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                chats:[
                    {src:"https://images.unsplash.com/photo-1549150712-1d243024db80?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8c3F1YXJlJTIwcG9ydHJhaXR8ZW58MHx8MHx8&auto=format&fit=crop&w=600&q=60", name:"Lutfhi Chan", date: "Jan 23, 2021"},
                    {src:"https://images.unsplash.com/photo-1542909168-82c3e7fdca5c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80", name:"Devi Carlos", date: "Jan 25, 2021"},
                    {src:"https://images.unsplash.com/photo-1549150712-1d243024db80?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8c3F1YXJlJTIwcG9ydHJhaXR8ZW58MHx8MHx8&auto=format&fit=crop&w=600&q=60", name:"Danar Comel", date: "Jan 21, 2021"},
                    {src:"https://images.unsplash.com/photo-1542909168-82c3e7fdca5c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80", name:"Lutfhi Chan", date: "Jan 25, 2021"},
                    {src:"https://images.unsplash.com/photo-1549150712-1d243024db80?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8c3F1YXJlJTIwcG9ydHJhaXR8ZW58MHx8MHx8&auto=format&fit=crop&w=600&q=60", name:"Karin Lumin", date: "Jan 19, 2021"},
                    {src:"https://images.unsplash.com/photo-1542909168-82c3e7fdca5c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80", name:"Fandid Deadan", date:"Jan 17, 2021"},
                ]
            }
        }
    }
</script>
<style>
    .discussion{
        margin-top:30px;
        background-color: white;
        padding:10px;
        border-radius: 10px;
        margin-bottom: 30px;
    }
    .chat{
        display: grid;
        grid-template-columns: 2fr 3fr 1fr;
        margin-bottom: 18px;
    }
    .chat p{
        font-size: 11px;
        font-weight: 500;
        color:#777;
    }
    .chat i{
        color: #999;
    }
</style>