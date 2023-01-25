<template>
  <div class="Feed container">
    <h3 class="header-text">Featured Wants</h3>
    <div class="container">
      <div class="row">
        <div v-for="(item, i) in items" :key="i" class="col card">
          <div :style="`background-image: url(${item.image})`" class="want-image">
          </div>
          <div class="found">
            {{item.found}} found
          </div>
          <div class="col card-description">
            <div class="item-name">
              {{ item.name }}
            </div>
            <div class="time">
              posted {{ item.datePosted }}
            </div>
            <div class="postedby">
              by <span class="user">{{ item.postedBy }}</span>
            </div>
            <div class="row interactions">
              <i class="icons"></i>
              <i class="icons"></i>
              <i class="icons"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Feed",
    data() {
      return {
        items: [
          {
            image: "https://m.media-amazon.com/images/I/71ifvqjRQLL._AC_SL1500_.jpg",
            found: "Not",
            name: "Smart Light Bars",
            datePosted: "a week ago",
            postedBy: "ChadChad125"
          },
          {
            image: "https://m.media-amazon.com/images/I/610PfXrRgKL._AC_SL1500_.jpg",
            found: "Similar Item",
            name: "Kitchen Faucet",
            datePosted: "a week ago",
            postedBy: "CK Pathak"
          },
          {
            image: "https://m.media-amazon.com/images/I/81xTjeYTw5L._SL1500_.jpg",
            found: "Exact Item",
            name: "Training Toothbrush Set",
            datePosted: "a week ago",
            postedBy: "Natalie"
          },
          {
            image: "https://m.media-amazon.com/images/I/61UdKFNc1QL._AC_UX522_.jpg",
            found: "Not",
            name: "Brady Men's Cotton Fleece",
            datePosted: "a week ago",
            postedBy: "Monteiro"
          },
          {
            image: "https://m.media-amazon.com/images/I/81I1DINyZHL._AC_UX679_.jpg",
            found: "Exact Item",
            name: "Citizen Men's Watch",
            datePosted: "a week ago",
            postedBy: "Song C."
          },
          {
            image: "https://m.media-amazon.com/images/I/51C6OnBxl-L._AC_UY575_.jpg",
            found: "Exact Item",
            name: "Oxfords Shoes",
            datePosted: "a week ago",
            postedBy: "Bruno Marc"
          },
          {
            image: "https://m.media-amazon.com/images/I/71t2q7l+nuS._AC_SL1500_.jpg",
            found: "Similar Item",
            name: "Wet Erase Markers",
            datePosted: "a week ago",
            postedBy: "Suzie Q"
          },
          {
            image: "https://m.media-amazon.com/images/I/61pP5gObVXL._SL1000_.jpg",
            found: "Exact Item",
            name: "CeraVe Moisturizing Cream",
            datePosted: "a week ago",
            postedBy: "Jen H."
          },
        ]
      }
    },
  };
</script>

<style scoped>
.container{
  width: 100%;
  background-color: #f1f0f0;
  padding: 0 20em;
}
.row{
  display: flex;
  flex-flow: wrap;
  place-content: space-evenly;
}
.col{
  display: flex;
  flex-direction: column;
  flex-shrink: 0;
}
.header-text{
  padding: 20px 0;
  font-size: 1.8rem;
  color: #8A8A8A;
  font-weight: 500;
  letter-spacing: 0.1rem;
  text-align: center;
}
.card{
  width: 230px;
  box-shadow: 0 0 10px 2px #d0d0d0;
  margin-bottom: 10px;
  border-radius: 4px;
  margin: 10px;
}
.want-image{
  height: 200px;
  background-color: white;
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
  border-radius: 5px;
  cursor: pointer;
  position: relative;
}
.want-image:hover::after{
  content: "View Want";
  width: 100%;
  height: 100%;
  background-color: rgba(12, 12, 12, 0.6);
  position: absolute;
  display: flex;
  display: flex;
  align-items: center;
  place-content: center;
  font-size: 1.8rem;
  font-weight: 500;
  color: white;
}
.card-description{
  text-align: center;
  line-height: 20px;
  padding: 5px 0;
}
.found{
  background-color: black;
  text-transform: uppercase;
  color: white;
  text-align: center;
  padding: 3px 0;
  font-size: 1.5rem;
}
.item-name{
  color: black;
  text-transform: capitalize;
  font-size: 1.4rem;
  font-weight: 500;
  cursor: pointer;
}
.time{
  color: gray;
  font-size: 1.3rem;
}
.postedby{
  font-size: 1.3rem;
  cursor: pointer;
}
.user{
  font-size: inherit;
  color: var(--vl-blue);
  font-weight: 500;
}
</style>