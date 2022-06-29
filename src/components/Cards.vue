<template>
    <div class="cards-container">
        <div v-for="card in cards">
            <div class="solo-card">
                <div class="text" >
                    <h3>{{card.num}}</h3>
                    <p>{{card.title}}</p>
                </div>
                <i :class="card.icon" :id="card.color"></i>
            </div>
        </div>
    </div>
</template>
<script>
export default{
    data(){
        return{
            cards:[
                {num: 720, title: "subscribers", icon:"fa fa-eye", color:"blue"},
                {num: 820, title: "Posts", icon:"fa fa-file", color:"purple"},
                {num: 920, title: "Pages", icon:"fa fa-file-text", color:"orange"},
                {num: 920, title: "Comments", icon:"fa fa-commenting", color:"green"},
            ]
        }
    },
}
</script>
<style>
    .cards-container{
        width:95%;
        margin:auto;
        display: flex;
        gap: 20px;
        margin-bottom: 30px;
    }
    .solo-card{
        background-color: white;
        padding: 15px;
        border-radius: 10px;
        display: grid;
        grid-template-columns: 3fr 1fr;
        color:#222;
        justify-content: space-between;
        align-items: center;

    }
    .text h3{
        margin-bottom: 10px;
    }
    .solo-card i{
        font-size: 20px important;
    }
    #blue, #purple, #green, #orange, #red{
        width:40px;
        height: 40px;
        display: inline-block;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    #blue{
        background-color: #dae1f2;
        color:var(--light-blue)
    }
      #purple{
        background-color: #deb0e5;
        color:#7c178c;
    }
    #orange{
        background-color: #ede2cb;
        color:#eaa315;
    }
    #green{
        background-color: #c9f2d3;
        color:#0bb736;
    }
    
    
</style>