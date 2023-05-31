<script>
import SmallCard from "./SmallCard.vue";
import BigCard from "./BigCard.vue";
import CustomersCard from "./CustomersCard.vue";
import ResendCarCard from "./ResendCarCard.vue";

export default {
  data() {
    return {
      activeIndex: 0,
      arrCategories: [
        "Cabrio",
        "Coupe",
        "Hatchback",
        "Pick Up",
        "Sedan",
        "SUV",
      ],
      arrBrands: ["BMW", "Seat", "Volswagen", "Mercedes-Benz", "Audi", "Fiat"],

      arrJumboImg: [
        {
          jumboImg: "../assets/img/slider-autocar-5.jpg",
        },
        {
          jumboImg: "../assets/img/slider-autocar-6.jpg",
        },
      ],
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
      arrCustomCard: [
        {
          customComment:
            "We are a gallery vehicle dealer. Before we met this site, our sales were sluggish.",
          customImg: "../assets/img/man1.png",
          customName: "Adam",
        },
        {
          customComment:
            "One of the quality websites I apply to rent a car. There are hundreds of different tools.",
          customImg: "../assets/img/testimonial2-1.png",
          customName: "Cristiane",
        },
        {
          customComment:
            "I was trying to sell my car. And I put it here and sold it for more than I was worth.",
          customImg: "../assets/img/man2.png",
          customName: "Robert",
        },
        {
          customComment:
            "A fast and reliable vehicle selling site. Rare quality website with hundreds of model vehicles.",
          customImg: "../assets/img/testimonial4-1.png",
          customName: "Elizabeth",
        },
      ],
      arrCustomCard2: [
        {
          customComment:
            "A fast and reliable vehicle selling site. Rare quality website with hundreds of model vehicles.",
          customImg: "../assets/img/man2.png",
          customName: "Adam",
        },
        {
          customComment:
            "I was trying to sell my car. And I put it here and sold it for more than I was worth.",
          customImg: "../assets/img/testimonial4-1.png",
          customName: "Cristiane",
        },
        {
          customComment:
            "One of the quality websites I apply to rent a car. There are hundreds of different tools.",
          customImg: "../assets/img/man1.png",
          customName: "Robert",
        },
        {
          customComment:
            "We are a gallery vehicle dealer. Before we met this site, our sales were sluggish.",
          customImg: "../assets/img/testimonial2-1.png",
          customName: "Elizabeth",
        },
      ],
      arrResendCar: [
        {
          resendImg: "../assets/img/news-autocar-1-300x180.jpg",
          resendBrand: "Why is BMW loved?",
          resendArticle:
            "BMWs have a different line with their designs and almost [...]",
        },
        {
          resendImg: "../assets/img/news-autocar-2-300x180.jpg",
          resendBrand: "How solid is Audi?",
          resendArticle:
            "According to Euro NCAP data with different test organization, there [...]",
        },
        {
          resendImg: "../assets/img/news-autocar-6-300x180.jpg",
          resendBrand: "What brand is Skoda?",
          resendArticle:
            "Skoda is one of the leading automotive manufacturers on the [...]",
        },
        {
          resendImg: "../assets/img/news-autocar-6-300x180.jpg",
          resendBrand: "Is the Auris diesel?",
          resendArticle:
            "You will have a quieter vehicle that burn less than [...]",
        },
      ],
    };
  },
  methods: {
    getImagePath(img) {
      return new URL(img, import.meta.url).href;
    },
    showNextSlide() {
      this.activeIndex++;

      if (this.activeIndex >= this.arrJumboImg.length) {
        this.activeIndex = 0;
      }
    },
    showPrevSlide() {
      this.activeIndex--;

      if (this.activeIndex < 0) {
        this.activeIndex = this.arrJumboImg.length - 1;
      }
    },
  },
  components: {
    SmallCard,
    BigCard,
    CustomersCard,
    ResendCarCard,
  },
};
</script>
<template>
  <main>
    <!-- JUMBOTRON -->
    <section>
      <div
        v-for="(element, index) in arrJumboImg"
        class="item"
        :key="element.jumboImg"
        :class="{ active: index == activeIndex }"
      >
        <img
          :src="getImagePath(element.jumboImg)"
          :alt="element.jumboImg"
          class="jumboImg"
        />
      </div>
      <div class="container">
        <div class="jumbo-details">
          <p class="jumbo-main">Buy And Sell Your Car At Its Value</p>
          <p class="jumbo-second">Find the right price and dealer.</p>
          <p class="jumbo-second">
            Learn More <font-awesome-icon icon="fa-solid fa-arrow-right" />
          </p>
        </div>
      </div>

      <div class="chevron left" @click="showPrevSlide">
        <font-awesome-icon icon="fa-solid fa-chevron-left" />
      </div>

      <div class="chevron right" @click="showNextSlide">
        <font-awesome-icon icon="fa-solid fa-chevron-right" />
      </div>
    </section>
    <!-- LISTA PER FILTRARE -->
    <section>
      <div class="container">
        <div class="filterChoose">
          <input type="text" placeholder="Keywords" class="text" />

          <input type="text" placeholder="Location" class="text" />

          <select>
            <option value="">All Categories</option>
            <option
              v-for="category in arrCategories"
              :key="category"
              :value="category"
            >
              {{ category }}
            </option>
          </select>

          <select>
            <option value="">Brand</option>
            <option v-for="brand in arrBrands" :key="brand" :value="brand">
              {{ brand }}
            </option>
          </select>

          <select>
            <option value="">Fuel Type</option>
          </select>

          <select>
            <option value="">Transmission</option>
          </select>

          <select>
            <option value="">Status</option>
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
        <div class="titleCustomers">
          <font-awesome-icon icon="fa-regular fa-thumbs-up" class="big-icon" />
          <div class="stars">
            <font-awesome-icon
              icon="fa-regular fa-star"
              v-for="star in 3"
              :key="star"
            />
          </div>
          <h2>What Are Our Customers Saying?</h2>
          <p>Opinions from our happy customers.</p>
        </div>

        <div class="customCards">
          <CustomersCard
            v-for="customCard in arrCustomCard2"
            :key="customCard.customName"
            :comment="customCard.customComment"
            :name="customCard.customName"
            :image="getImagePath(customCard.customImg)"
          />
        </div>
      </div>
    </section>
    <!-- ARTICOLI MARCHE MACCHINE -->
    <section>
      <div class="container">
        <div class="resent-articles">
          <div class="resent-title">
            <div class="like">
              <font-awesome-icon icon="fa-solid fa-thumbs-up" />
            </div>
            <h2>Resent Articles</h2>
            <p>Useful information about car.</p>
          </div>

          <div class="resent-cards">
            <ResendCarCard
              v-for="resendCar in arrResendCar"
              :key="resendCar.resendBrand"
              :img="getImagePath(resendCar.resendImg)"
              :brand="resendCar.resendBrand"
              :article="resendCar.resendArticle"
            />
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<style lang="scss" scoped>
@use "../assets/partials/variables" as *;
.item.active {
  display: block;
}
.item {
  display: none;
  height: 100vh;
  .jumboImg {
    width: 100%;
    height: 100%;
    object-fit: cover;
    position: relative;
  }
}
.chevron {
  color: $white-main;
  font-size: 2rem;
  &.left {
    position: absolute;
    top: 50%;
    left: 10px;
    &:hover {
      cursor: pointer;
    }
  }
  &.right {
    position: absolute;
    top: 50%;
    right: 10px;
    &:hover {
      cursor: pointer;
    }
  }
}
.jumbo-details {
  color: $white-main;
  position: absolute;
  top: 50%;
  left: 10%;
  .jumbo-main {
    font-size: 3rem;
    font-weight: 800;
    max-width: 500px;
  }
  .jumbo-second {
    font-size: 1rem;
    font-weight: 600;
    line-height: 30px;
  }
}

.filterChoose {
  display: flex;
  padding: 1rem;
  gap: 1rem;
  input {
    width: calc((100% - 7rem) / 8);
    padding: 1.5rem;
    border-radius: 5px;
  }
  select {
    width: calc((100% - 7rem) / 8);
    padding: 1.5rem;
    border-radius: 5px;
  }
  button {
    width: calc((100% - 7rem) / 8);
    padding: 1.5rem;
    background-color: $black-main;
    color: $white-main;
    font-weight: 600;
    border-radius: 5px;
  }
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
      color: $white-main;
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
  .titleCustomers {
    color: white;
    text-align: center;
    padding-top: 3rem;
    .big-icon {
      font-size: 3rem;
    }
    h2 {
      margin-top: 1.5rem;
      margin-bottom: 1rem;
      font-size: 1.5rem;
      font-weight: 700;
    }
  }
  .customCards {
    display: flex;
    gap: 1rem;
    margin-top: 3rem;
  }
}

// PROVA PER CAROSELLO

.resent-articles {
  text-align: center;
  .resent-title {
    display: flex;
    flex-direction: column;
    align-items: center;
    .like {
      color: $white-main;
      background-color: $black-main;
      width: 90px;
      height: 90px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3rem;
      margin-top: 5rem;
    }
    h2 {
      margin: 1rem 0;
      font-size: 1.5rem;
      font-weight: 800;
    }
    p {
      margin-bottom: 1rem;
      font-size: 0.8rem;
    }
  }
  .resent-cards {
    display: flex;
    gap: 3rem;
  }
}
</style>
