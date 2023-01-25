<template>
  <div class="hero">
    <div class="row">
      <div class="col">
        <h2 class="hero-text">
          Add the products you want.<br/>
          Get local prices in under
          <span class="time">24 hours!*</span>
        </h2>
        <button class="gold">Add a product you're looking for?</button>
      </div>
      <div class="col">
        <img class="imageBox" src="../assets/pngegg.png"/>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "HeroSection",
  };
</script>

<style scoped>
.hero{
  width:100%;
  height: 200em;
  background-image: url(../assets/map.jpg);
  background-size: cover;
  color: black;
  background-color: rgb(202, 9, 202);
  background-blend-mode: lighten;
}
.row{
  display: flex;
  flex-direction: row;
  height: 100%;
  align-items: center;
  justify-content: space-around;
  background: rgba(255, 255, 255, 0.7);
  background-position: center;
}
.col{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.hero-text, .time{
  font-size: 3rem;
  line-height: 1.5em;
  font-weight: 500;
}
.time{
  color: var(--vl-blue);
}
.gold{
  background-color: #FBB726;
  color: white;
  border: 1px  solid#bd8a1c;
  font-size: 1.6rem;
  padding: 5px 10px;
  box-shadow: 1px 2px #bd8a1c;
  border-radius: 4px;
  margin-top: 5px;
}
.imageBox{
  height: 100%;
}
</style>
