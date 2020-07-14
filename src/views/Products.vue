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
            class="card-img-top"
            src="https://mdbootstrap.com/img/Photos/Others/images/43.jpg"
            alt="Card image cap"/>

          <!-- Card content -->
          <div class="card-body">
            <!-- Title -->
            <h4 class="card-title">
              <a>Card title</a>
            </h4>
            <!-- Text -->
            <p class="card-text">
              Some quick example text to build on the card title and make up the bulk of the card's
              content.
            </p>
            <!-- Button -->
            <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#fullHeightModalRight">ADD TO CART</button>
          </div>
        </div>
      </div>

      <!-- NOTE ITEM 2 -->
      <div class="col-2">
        <div class="card">
          <!-- Card image -->
          <img
            class="card-img-top"
            src="https://mdbootstrap.com/img/Photos/Others/images/43.jpg"
            alt="Card image cap"
          />

          <!-- Card content -->
          <div class="card-body">
            <!-- Title -->
            <h4 class="card-title">
              <a>Card title</a>
            </h4>
            <!-- Text -->
            <p class="card-text">
              Some quick example text to build on the card title and make up the bulk of the card's
              content.
            </p>
            <!-- Button -->
            <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#fullHeightModalRight">ADD TO CART</button>
          </div>
        </div>
      </div>

      <!-- NOTE ITEM 3 -->
      <div class="col-2">
        <div class="card">
          <!-- Card image -->
          <img
            class="card-img-top"
            src="https://mdbootstrap.com/img/Photos/Others/images/43.jpg"
            alt="Card image cap"
          />

          <!-- Card content -->
          <div class="card-body">
            <!-- Title -->
            <h4 class="card-title">
              <a>Card title</a>
            </h4>
            <!-- Text -->
            <p class="card-text">
              Some quick example text to build on the card title and make up the bulk of the card's
              content.
            </p>
            <!-- Button -->
        <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#fullHeightModalRight">ADD TO CART</button>
          </div>
        </div>
      </div>


      <!-- NOTE ITEM 4 -->
      <div class="col-2">
        <div class="card">
          <!-- Card image -->
          <img
            class="card-img-top"
            src="https://mdbootstrap.com/img/Photos/Others/images/43.jpg"
            alt="Card image cap"
          />

          <!-- Card content -->
          <div class="card-body">
            <!-- Title -->
            <h4 class="card-title">
              <a>Card title</a>
            </h4>
            <!-- Text -->
            <p class="card-text">
              Some quick example text to build on the card title and make up the bulk of the card's
              content.
            </p>
            <!-- Button -->
            <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#fullHeightModalRight">ADD TO CART</button>
          </div>
        </div>
      </div>

    </div>

<!-- NOTE SHOPPING CART MODAL -->
<div class="modal fade right" id="miniCart" tabindex="-1" role="dialog" aria-labelledby="myModalLabel"
  aria-hidden="true">

  <!-- Add class .modal-full-height and then add class .modal-right (or other classes from list above) to set a position to the modal -->
  <div class="modal-dialog modal-full-height modal-right" role="document">


    <div class="modal-content">
      <div class="modal-header">
        <h4 class="modal-title w-100" id="myModalLabel">My Cart</h4>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        ...
      </div>
      <div class="modal-footer justify-content-center">
        <button type="button" class="btn btn-secondary" data-dismiss="modal">Continue Shopping</button>
        <button type="button" class="btn btn-primary">Checkout</button>
      </div>
    </div>
  </div>
</div>
<!-- Full Height Modal Right -->

  </div>
</template>


<script>
export default {
  name: "Products",
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {}
};
</script>


<style scoped>
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
</style>