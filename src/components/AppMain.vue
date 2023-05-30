<script>
import SmallCard from "./SmallCard.vue";
import BigCard from "./BigCard.vue";

export default {
  data() {
    return {
      arrSmallCard: [
        {
          type: "Cabrio",
          img: "../assets/img/cabrio.jpg",
        },
        {
          type: "Coupe",
          img: "../assets/img/coupe.jpg",
        },
        {
          type: "Hatchback",
          img: "../assets/img/hatchback.jpg",
        },
        {
          type: "Pick Up",
          img: "../assets/img/pickup.jpg",
        },
        {
          type: "Sedan",
          img: "../assets/img/sedan.jpg",
        },
        {
          type: "SUV",
          img: "../assets/img/suv.jpg",
        },
      ],
      arrBigCard: [
        {
          carName: "BMW M9",
          carType: "Cabrio",
          carPrice: "34,000",
          carBrand: "BMW",
          carFuel: "Electric",
          carThumb:
            "../assets/img/bmw-8-series-convertible-technical-data-sp-desktop-400x300.jpg",
        },
        {
          carName: "BMW M8",
          carType: "Cabrio",
          carPrice: "34,000",
          carBrand: "BMW",
          carFuel: "Diesel",
          carThumb: "../assets/img/bmw88-400x300.jpg",
        },
        {
          carName: "BMW 4",
          carType: "Cabrio",
          carPrice: "34,000",
          carBrand: "BMW",
          carFuel: "Gasoline",
          carThumb: "../assets/img/bmw442-400x300.jpg",
        },
        {
          carName: "Seat Ibiza",
          carType: "Hatchback",
          carPrice: "27,000",
          carBrand: "Seat",
          carFuel: "Electric",
          carThumb: "../assets/img/yeni-ibiza-2-400x300.jpg",
        },
        {
          carName: "Seat Arona",
          carType: "SUV",
          carPrice: "68,000",
          carBrand: "Seat",
          carFuel: "Gasoline",
          carThumb: "../assets/img/makyajli-2022-seat-arona-1-400x300.jpg",
        },
        {
          carName: "Volswagen Taigo",
          carType: "SUV",
          carPrice: "52,000",
          carBrand: "Volswagen",
          carFuel: "Electric",
          carThumb: "../assets/img/vw-taigo3832-400x300.jpg",
        },
        {
          carName: "Volswagen T-Cross",
          carType: "SUV",
          carPrice: "47,000",
          carBrand: "Volswagen",
          carFuel: "Diesel",
          carThumb: "../assets/img/2019-vw-t-cross-400x300.jpg",
        },
        {
          carName: "Volswagen Passat",
          carType: "Sedan",
          carPrice: "32,000",
          carBrand: "Volswagen",
          carFuel: "Diesel",
          carThumb: "../assets/img/volkswagen-passat-1280x720-1-400x300.jpg",
        },
      ],
    };
  },
  methods: {
    getImagePath(img) {
      return new URL(img, import.meta.url).href;
    },
  },
  components: {
    SmallCard,
    BigCard,
  },
};
</script>
<template>
  <main>
    <!-- JUMBOTRON -->
    <section class="jumbo">
      <div class="container">
        <div class="jumbo-details">
          <p class="jumbo-main">Buy And Sell Your Car At Its Value</p>
          <p class="jumbo-second">Find the right price and dealer.</p>
          <p class="jumbo-second">Learn More -></p>
          <!--AGGIUNGERE ICONA FRECCIA -->
        </div>
      </div>
    </section>
    <!-- LISTA PER FILTRARE -->
    <section>
      <div class="container">
        <div class="filterChoose">
          <input type="text" placeholder="Keywords" />

          <input type="text" placeholder="Location" />

          <select>
            <option value="">All Categories</option>
          </select>

          <select>
            <option value="">Brand</option>
          </select>

          <select>
            <option value="">Fuel Type</option>
          </select>

          <select>
            <option value="">Transmission</option>
          </select>

          <select>
            <option value="">Form</option>
          </select>

          <button>Search</button>
        </div>
      </div>
    </section>
    <!-- CARDS PER FILTRARE CON IMMAGINE -->
    <section>
      <div class="container">
        <div class="smallCardList">
          <SmallCard
            v-for="smallCards in arrSmallCard"
            :key="smallCards.type"
            :carType="smallCards.type"
            :urlImg="getImagePath(smallCards.img)"
          />
        </div>
      </div>
    </section>
    <!-- CARDS DELLE AUTO -->
    <section>
      <div class="container">
        <div class="carShop">
          <BigCard
            v-for="bigCard in arrBigCard"
            :key="bigCard.carName"
            :name="bigCard.carName"
            :type="bigCard.carType"
            :price="bigCard.carPrice"
            :brand="bigCard.carBrand"
            :fuel="bigCard.carFuel"
            :imgUrl="getImagePath(bigCard.carThumb)"
          />
        </div>
        <div class="showMore">
          Show All Cars <font-awesome-icon icon="fa-solid fa-arrow-right" />
        </div>
      </div>
    </section>

    <!-- VUOI VENDERE LA TUA AUTO? -->
    <section>
      <div class="container-small">
        <div class="contents">
          <div class="car-left">
            <img src="../assets/img/aoutcar-about-1.png" alt="Auto about" />
            <div class="about top">
              <p class="number">2 4</p>
              <p>Years of Experience</p>
            </div>

            <div class="about bottom">
              <p class="number">2 4 0</p>
              <p>Special Expert Team</p>
            </div>
          </div>
          <div class="info-right">
            <h2>Whant to buy or sell a vehicle?</h2>
            <p>
              You can put your vehicles for sale by registering on our website.
              Whether you are a dealer or sell personally. Sell your vehicle in
              the most profitable way. With this system, which has millions of
              members, you will be able to buy and sell vehicles very quickly.
            </p>
            <img src="../assets/img/divider.jpg" alt="divider" />
            <div class="vehicles">
              <font-awesome-icon icon="fa-solid fa-car" class="car-icon" />
              <div class="know-us">
                <h3>Model Vehicles</h3>
                <p>
                  We are sure that you will find vehicles of suitable models on
                  our website.
                </p>
              </div>
            </div>

            <div class="vehicles">
              <font-awesome-icon icon="fa-solid fa-car" class="car-icon" />
              <div class="know-us">
                <h3>2nd Hand Vehicles</h3>
                <p>
                  You can put your used vehicles for sale by adding them to our
                  website.
                </p>
              </div>
            </div>

            <div class="know-btn">
              Get to know us
              <font-awesome-icon icon="fa-solid fa-arrow-right" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- RECENSIONI CLIENTI -->
    <section class="customers">
      <div class="container">
        <div class="titleCustomers"></div>
      </div>
    </section>
  </main>
</template>

<style lang="scss" scoped>
@use "../assets/partials/variables" as *;

.jumbo-details {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 0.8rem;
}
.jumbo {
  height: 100vh;
  background-image: url(../assets/img/slider-autocar-5.jpg);
  background-size: cover;
  color: $white-main;
  .jumbo-main {
    font-size: 3rem;
    font-weight: 800;
    max-width: 500px;
  }
  .jumbo-second {
    font-size: 1.3rem;
    font-weight: 600;
  }
}

.filterChoose {
  display: flex;
  justify-content: space-between;
  padding: 0.5rem;
}

.smallCardList {
  display: flex;
  padding-bottom: 1rem;
}

.carShop {
  display: flex;
  flex-wrap: wrap;
}

.showMore {
  background-color: $black-main;
  padding: 1rem;
  text-align: center;
  color: $white-main;
  font-weight: 700;
  width: 200px;
  margin-inline: auto;
  &:hover {
    cursor: pointer;
  }
}

.contents {
  display: flex;
  gap: 2rem;
  height: 100vh;
  margin-top: 5rem;
  margin-bottom: 5rem;
  .car-left {
    background-image: url(../assets/img/circle-auto-car-1.png);
    background-size: cover;
    position: relative;
    .about {
      background-color: $black-main;
      color: $white-main;
      text-align: center;
      width: 150px;
      height: 150px;
      font-weight: 800;
      border-radius: 50rem;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      .number {
        font-size: 2rem;
      }
      &.top {
        position: absolute;
        top: 100px;
        left: 70px;
      }

      &.bottom {
        position: absolute;
        bottom: 140px;
        right: 50px;
      }
    }
  }
  .info-right {
    h2 {
      font-size: 1.8rem;
      padding-top: 5rem;
      padding-bottom: 1rem;
    }
    p {
      line-height: 30px;
    }
    img {
      margin-top: 1rem;
      margin-bottom: 1rem;
    }
    .vehicles {
      display: flex;
      gap: 0.7rem;
      margin-bottom: 2rem;
      .car-icon {
        font-size: 4rem;
      }
      h3 {
        margin-bottom: 0.7rem;
        font-size: 1.5rem;
        font-weight: 700;
      }
    }
    .know-btn {
      width: 300px;
      color: white;
      font-weight: 700;
      text-align: center;
      background-color: $black-main;
      padding: 1.5rem 2rem;
      &:hover {
        cursor: pointer;
      }
    }
  }
}

.customers {
  height: 100vh;
  background-image: url(../assets/img/comment-bg-autocar.jpg);
  background-size: cover;
}
</style>
