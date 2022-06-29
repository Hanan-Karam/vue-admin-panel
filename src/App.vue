<script>
import Avatar from '@/components/Avatar.vue';
import Cards from '@/components/Cards.vue';
import Devices from '@/components/Devices.vue';
import Discussion from '@/components/Discussion.vue';
import LeftSide from '@/components/LeftSide.vue';
import Search from '@/components/Search.vue';
import TopReferals from '@/components/TopReferals.vue';
import Users from '@/components/Users.vue';
import Viewers from '@/components/Viewers.vue';
export default{
  components:{
    Avatar,
    Cards,
    Devices,
    Discussion,
    LeftSide,
    Search,
    TopReferals,
    Users,
    Viewers
  }
}
</script>

<template>
  <w-app>
  <div class="container">
    <div class="left">
      <LeftSide/>
    </div>
    <div class="middle">
      <Search/>
      <Cards/>
      <Users/>
      <div class="middle--bottom">
        <TopReferals/>
        <Viewers/>
      </div>
    </div>
    <div class="right">
      <Avatar/>
      <Discussion/>
      <Devices/>
    </div>
  </div>
</w-app>
</template>

<style>
:root{
  --bg-color: #c9d5e5;
  --body-font: 'Montserrat', sans-serif;
  --light-blue: #009bd5;
  --menue-text: #adbad6;
}
body{
  background-color: var(--bg-color);
  font-family: var(--body-font);
}
.container{
  width: 80%;
  margin: auto;
  height: 80%;
  display: grid;
  grid-template-columns: 1fr 3fr 1fr;
  background-color: #ecf1f9;
  border-radius:20px;
  padding-right: 30px;
}
.middle--bottom{
  width:95%;
  margin: 30px auto 0;
  display: flex;
  gap:30px;
}
.middle{
  margin:0 30px 30px 30px;
}
.right{
  margin-right:30px;
  margin-bottom: 30px;
}


</style>
