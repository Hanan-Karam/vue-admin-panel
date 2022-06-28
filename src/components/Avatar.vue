<template>
<div class="avatar">
    <div class="notification">
        <w-badge class="mr10" overlap xs bg-color="error">
            <template #badge>3</template>
            <i class="fa fa-bell" aria-hidden="true"></i>
        </w-badge>
    </div>
    <div>
        <img 
            src="https://images.unsplash.com/photo-1542909168-82c3e7fdca5c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80" 
            alt=""
        >
    </div>
    <div><p>Hii, Arinales</p></div>
</div>
</template>
<style>
    .avatar{
        display: grid;
        grid-template-columns: 1fr 1fr 2fr;
        justify-content: space-between;
        align-items: center;
        margin-top: 30px;
        margin-left:10px;
    }
    img{
        border-radius: 50%;
        width:30px;
    }
    p{
        font-size: 12px;
        font-weight: bold;
    }
</style>