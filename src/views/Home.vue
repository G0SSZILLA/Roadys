
<template>
  <div class="Home container-fluid">
<div class="row roadysImg" style="height:550px"></div>
<div class="row products">

  <!-- NOTE CARD 1 -->
  <div class="col-3">
<div class="card card-cascade wider  bg-transparent border-0">

  <!-- Card image -->
  <div class="view view-cascade overlay">
    <img class="card-img-top shadow" src="../assets/diesel.png" alt="Card image cap">
    <a href="#!">
      <div class="mask rgba-white-slight"></div>
    </a>
  </div>

  <!-- Card content -->
  <div class="card-body card-body-cascade pr-0 text-center">

    <!-- Title -->
    <h4 class="card-title"><strong>Fuel</strong></h4>
    
    <!-- Text -->
    <p class="card-text">Skip the long lines elsewhere. Reduced wait times, low prices and great amenities make Roady's the perfect place to fuel up. </p>

  <a class="btn btn-btn buttonCard-1 shadow">Find Fuel</a>

  </div>

</div>
  </div>

  <!-- NOTE CARD 2 -->
  <div class="col-3">
<div class="card card-cascade wider bg-transparent border-0">

  <!-- Card image -->
  <div class="view view-cascade overlay">
    <img class="card-img-top shadow" src="../assets/burger.png" alt="Card image cap">
    <a href="#!">
      <div class="mask rgba-white-slight"></div>
    </a>
  </div>

  <!-- Card content -->
  <div class="card-body card-body-cascade text-center">

    <!-- Title -->
    <h4 class="card-title"><strong>Food</strong></h4>
   
    <!-- Text -->
    <p class="card-text">Roady's prides ourselves on having some of the best home cooked food on the interstate. Friendly staff, great food and affordable prices. </p>

    <a class="btn btn-unique buttonCard shadow">Find Food</a>

  </div>

</div>
  </div>

<!-- NOTE CARD 3 -->
  <div class="col-3 ">
<div class="card card-cascade wider bg-transparent border-0">

  <!-- Card image -->
  <div class="view view-cascade overlay">
    <img class="card-img-top shadow" src="../assets/shower.png" alt="Card image cap">
    <a href="#!">
      <div class="mask rgba-white-slight"></div>
    </a>
  </div>

  <!-- Card content -->
  <div class="card-body card-body-cascade text-center">

    <!-- Title -->
    <h4 class="card-title"><strong>Shower</strong></h4>
   
    <!-- Text -->
    <p class="card-text">Wash away the miles. Earn a free shower credit on your Roady's Reward card with the purchace of 50 gallons or more of fuel.</p>

   <a class="btn btn-unique buttonCard shadow">Find Showers</a>

  </div>

</div>
  </div>

<!-- NOTE CARD 4 -->
  <div class="col-3 p-0 ">
<div class="card card-cascade wider  bg-transparent border-0">

  <!-- Card image -->
  <div class="view view-cascade overlay">
    <img class="card-img-top serviceImg shadow" src="../assets/service.png" alt="Card image cap">
    <a href="#!">
      <div class="mask rgba-white-slight"></div>
    </a>
  </div>

  <!-- Card content -->
  <div class="card-body card-body-cascade text-center">

    <!-- Title -->
    <h4 class="card-title"><strong>Service</strong></h4>
  
    <!-- Text -->
    <p class="card-text ">Need repair? Roady's Service Centers offer national coverage to meet all your needs. Let our pros help you get back on the road fast.</p>

  <a class="btn btn-unique buttonCard shadow">Find Service Centers</a>

  </div>

</div>
  </div>
</div>

<!-- NOTE REWARDS -->
<div class="row register mr-0">
</div>

<div class="row upgrade">
  <div class="col-2"></div>
<div class="col-4 pl-0 roadyText">
    <h1 class="pb-2 readyForReward">Ready for a Reward Upgrade?</h1>
    <h2 class="pb-2 morePoints">MORE POINTS, MORE PRIZES, AND MORE WAYS TO REDEEM!</h2>
    <p class="pb-2 getRewarded">Get rewarded for being a Roady's customer! With the launch of our app, there are more ways than ever to earn points as a member, plus brand new giveaways and sweepstakes.</p>
</div>
<div class="col-1"></div>
<div class="col-5 roadyCard"></div>
</div>
<div class="row btnRow">
  <div class="col-4 text-right"><a class="btn btn-unique rewardBtn shadow">LEARN MORE</a></div>
  <div class="col-4 text-center"><a class="btn btn-unique rewardBtn shadow">REGISTER YOUR CARD</a></div>
  <div class="col-4 text-left"><a class="btn btn-unique rewardBtn shadow">CHECK BALANCE</a></div>
</div>
<div class="row knowATruckstop"></div>

  </div>
</template>


<script>
export default {
  name: 'Home',
  data(){
    return {}
  },
  computed:{},
  methods:{},
  components:{}
}
</script>


<style scoped>
/* * {
    margin: 0px !important;
    padding: 0px !important;
    box-sizing: border-box !important;
} */

.roadysImg{
  background-image: url(https://roadys.com/wp-content/uploads/2018/03/becomeARoadys.jpg);
  background-position: center;
  width: 99vw;
}
.products{
  background-color:#1e549a ;
  height: 550px;
  
}
.card{
  color: aliceblue;
  width: 483px;
  font-weight: 500;
}
.card-title{
  text-align: start;
  font-size: 35px;
}

.card-text{
  text-align: start;
  font-size: 1rem;
  
}

.card-img-top{
  width: 475.5px;
  height: 250px;
}

.serviceImg{
  width: 475.5px;
}

.buttonCard-1{
  margin-top: 97px;
  background-color:#12325c;
  width: 300px;
  font-size: 1.25rem;
  font-weight: 700;
}

.buttonCard{
  margin-top: 75px;
  background-color:#12325c;
  width: 300px;
  font-size: 1.25rem;
  font-weight: 700;
}

.register{
  background-image: url(https://roadys.com/wp-content/uploads/2019/06/rewards__3_.png);
  background-size: 900px;
  background-position: center;
  background-repeat: no-repeat;
  height: 550px;
  width: 99vw;
  
}

.upgrade{
  height: 550px;
}

.roadyCard{
  background-image: url(https://roadys.com/wp-content/uploads/2018/07/CardReflection.jpg);
   background-size: 500px;
  margin-top: 50px;
  background-repeat: no-repeat;
}

.roadyText{
  text-align: start;
  margin-top: 150px;
}

.readyForReward{
font-weight: 800;
font-size: 2.7rem;
}

.morePoints{
  font-weight: 400;
}

.getRewarded{
  font-size: 18px;
}

.rewardBtn{
  font-weight: 500;
  background-color: #f3f3f3;
}
.btnRow{
  height: 100px;
}

.knowATruckstop{
  background-color:#1e549a ;
  height: 550px;
  
}
</style>
