<template>
  <div class="Products">
    <div class="row roadyProductImg"></div>

    <!-- NOTE PRODUCT NAV -->
    <div class="row productNav">
      <div class="col-2"></div>
      <div class="col-2">
        <h2 class="mt-4 navText text-white">All Products</h2>
      </div>
      <div class="col-2">
        <h2 class="mt-4 navText text-white">Candy</h2>
      </div>
      <div class="col-2">
        <h2 class="mt-4 navText text-white">Gas</h2>
      </div>
      <div class="col-2">
        <h2 class="mt-4 navText text-white">Misc.</h2>
      </div>
      <div class="col-2 text-center mt-3 pl-5">
    
          <button type="button" class="btn btn-primary cartText" data-toggle="modal" data-target="#fullHeightModalRight"> CART 
              <img class="mb-1" src="https://img.icons8.com/material/24/000000/buy--v1.png" /></button>

      </div>
    </div>

    <div class="row itemsRow pl-5">

        <!-- NOTE ITEM 1 -->
      <div class="col-2">
        <div class="card">
          <!-- Card image -->
          <img
            class="card-img-top snickers"
            src="../assets/Screen-Shot-2019-11-04-at-4.49.46-PM_600x.png"
            alt="Card image cap"/>

          <!-- Card content -->
          <div class="card-body">
            <!-- Title -->
            <h4 class="card-title">
              <a>Snickers</a>
            </h4>
            <!-- Text -->
            <p class="card-text">
              A yummy delicous chocolate bar with peanuts and carmel.
            </p>
            <!-- Button -->
            <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#fullHeightModalRight" @click="addToCart">ADD TO CART</button>
          </div>
        </div>
      </div>

      <!-- NOTE ITEM 2 -->
      <div class="col-2">
        <div class="card">
          <!-- Card image -->
          <img
            class="card-img-top mt-5 pt-5"
            src="../assets/rockyroad.png"
            alt="Card image cap"
          />

          <!-- Card content -->
          <div class="card-body">
            <!-- Title -->
            <h4 class="card-title mt-5">
              <a>Rocky Road</a>
            </h4>
            <!-- Text -->
            <p class="card-text">
              Rocky road ice cream in candy bar form.
            </p>
            <!-- Button -->
            <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#fullHeightModalRight" @click="addToCart">ADD TO CART</button>
          </div>
        </div>
      </div>

      <!-- NOTE ITEM 3 -->
      <div class="col-2">
        <div class="card">
          <!-- Card image -->
          <img
            class="card-img-top reeses"
            src="../assets/reeses.png"
            alt="Card image cap"
          />

          <!-- Card content -->
          <div class="card-body">
            <!-- Title -->
            <h4 class="card-title">
              <a>Reeses cups</a>
            </h4>
            <!-- Text -->
            <p class="card-text">
              Perfect combo of chocolate and peanutbutter
            </p>
            <!-- Button -->
        <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#fullHeightModalRight" @click="addToCart">ADD TO CART</button>
          </div>
        </div>
      </div>


      <!-- NOTE ITEM 4 -->
      <div class="col-2">
        <div class="card">
          <!-- Card image -->
          <img
            class="card-img-top nerds mt-5"
            src="../assets/1_j5pfQasjr3S_lZxEc5eAbA.png"
            alt="Card image cap"/>

          <!-- Card content -->
          <div class="card-body">
            <!-- Title -->
            <h4 class="card-title">
              <a>Nerds</a>
            </h4>
            <!-- Text -->
            <p class="card-text">
              Tangy, crunchy candy, a willy wonka classic!
            </p>
            <!-- Button -->
            <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#fullHeightModalRight" @click="addToCart">ADD TO CART</button>
          </div>
        </div>
      </div>
    </div>

<!-- NOTE SHOPPING CART MODAL -->
<div class="modal fade right" id="fullHeightModalRight" tabindex="-1" role="dialog" aria-labelledby="myModalLabel"
  aria-hidden="true">

  <div class="modal-dialog modal-full-height modal-right" role="document">


    <div class="modal-content">
      <div class="modal-header">
        <h4 class="modal-title w-100" id="myModalLabel">My Cart</h4>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        <ul>
            <li :v-for="item in this.$store.state.cart">
                <span>{{this.productName}}</span>
                <span>{{item.productPrice}}</span>
                <span>{{item.productDescription}}</span>
                <span class="quantity"> <button class="quantityMinus mr-2" @click="addToQuantity">&minus;</button>{{item.productQuantity}}<button class="quantityPlus ml-2" @click="removeQuantity">&plus;</button></span>
            </li>
        </ul>
        <hr>
      </div>
      <div class="modal-footer justify-content-center">
        <button type="button" class="btn btn-secondary" data-dismiss="modal">Continue Shopping</button>
        <button type="button" class="btn btn-primary">Checkout</button>
      </div>
    </div>
  </div>
</div>


  </div>
</template>


<script>
export default {
  name: "Products",
  props:{
      name:String,
      price:Number,
      description:String,
      quantity:Number,
  },
  data() {
    return {
        item:{
            productName:this.name,
            productPrice: this.price,
            productDescription: this.description,
            productQuantity: 1,
        }
    };
  },
  computed: {},
  methods: {
      addToCart(){
          this.$store.commit('addToCart', this.item)
      },
      addToQuantity(){
          this.productQuantity += this.productQuantity
      },
      removeQuantity(){
          this.productQuantity -= this.productQuantity
      }
  },
  components: {}
};
</script>


<style scoped>

.snickers{
height: 100.72;
}

.cartText {
  font-weight: 600;
  font-size: 18px;
}

.itemsRow {
  margin-top: 50px;
}

.navText {
  text-align: center;
  font-size: 1.5rem;
}
.roadyProductImg {
  background-position: 0 -600px;
  background-image: url(http://roadys.wpengine.com/wp-content/uploads/2018/03/becomeAVendor.jpg);
  height: 350px;
}

.productNav {
  height: 75px;
  background-color: #1e549a;
}

.quantity{
border: 3px;
}

.quantityMinus{

}
</style>