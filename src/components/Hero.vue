<template>
  <div class="hero">
    <!-- Dekstop -->
    <div class="d-md-block d-none">
      <div
        class="row mt-4 d-flex justify-content-center align-items-center">
        <div class="col-md-6">
          <div class="justify-content-center align-self-center">
            <h2>
              <strong>Delicious Foods, </strong> <br />in Your
              Gadgets
            </h2>
            <p>Hurry up and order your favourite food!</p>
            <button class="btn btn-lg btn-warning">
              <b-icon-arrow-right></b-icon-arrow-right> Order
            </button>
          </div>
        </div>
        <div class="col-md-6">
          <img
            src="../assets/images/hero.svg"
            alt=""
            width="100%" />
        </div>
      </div>
    </div>

    <!-- Mobile  -->
    <div class="d-sm-block d-md-none">
      <div
        class="row mt-4 d-flex justify-content-center align-items-center">
        <div class="col-md-6 mb-3">
          <img
            src="../assets/images/hero.svg"
            alt=""
            width="100%" />
        </div>
        <div class="col-md-6">
          <div class="justify-content-center align-self-center">
            <h2>
              <strong>Delicious Foods, </strong> <br />in Your
              Gadgets
            </h2>
            <p>Hurry up and order your favourite food!</p>
            <button class="btn btn-lg btn-warning">
              <b-icon-arrow-right></b-icon-arrow-right> Order
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeroSection",
};
</script>

<style></style>
