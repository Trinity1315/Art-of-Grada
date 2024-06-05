<template>
  <nav>
    <div class="navbar-container" style="margin-top: -40px;">
      <div class="navbar-brand">
        <img class="navbar-brand-logo" src="resources/logo.png" alt="Logo">
        <a class="navbar-brand-name" href="index.html">ART OF GRADA</a>
      </div>
      <div class="navbar-collapse">
        <div class="navbar-search">
          <div class="search-box">
            <i class="fa fa-search"></i>
            <input type="text" placeholder="Search">
          </div>
        </div>
        <div class="navbar-items">
          <ul>
            <li class="dropdown">
              <a id="dropdownToggleProfile"><i class="fas fa-user"></i></a>
              <div class="dropdown-content-profile">
                <a href="login.html">
                  <i class="fab fa-ethereum"></i>
                  <span>Login</span>
                </a>
                <a href="profile.html">
                  <i class="fas fa-user-circle"></i>
                  <span>Profile</span>
                </a>
                <a href="profile.html">
                  <i class="fas fa-thumbs-up"></i>
                  <span>Liked</span>
                </a>
                <a href="profile.html">
                  <i class="fas fa-wallet"></i>
                  <span>Owned</span>
                </a>
              </div>
            </li>
            <li class="dropdown">
              <a id="dropdownToggleCalculator"><i class="fas fa-calculator"></i></a>
              <div class="dropdown-content-calculator">
                <div class="calculator-container">
                  <div class="calculator-inputs">
                    <input type="number" placeholder="Enter amount" id="currency-input">
                    <i class="fab fa-ethereum"></i>
                  </div>
                  <div class="calculator-inputs">
                    <input type="number" placeholder="Result" id="currency-output" readonly>
                    <select id="currency-select">
                      <option value="kzt">KZT</option>
                      <option value="usdt">USDT</option>
                      <option value="rub">RUB</option>
                    </select>
                  </div>
                </div>
              </div>
            </li>
            <li>
              <a href="create.html"><i class="fas fa-plus"></i></a>
            </li>
            <li class="dropdown">
              <a id="dropdownToggleCart">
                <i class="fas fa-shopping-cart" style="-webkit-text-stroke: 1px rgb(255, 255, 255);color: transparent;"></i>
              </a>
              <div class="dropdown-content-cart">
                <div class="cart-card-header">
                  <h1>Your Cart</h1>
                  <a><i class="fas fa-times"></i></a>
                </div>
                <div class="cart-card-items">
                  <h3>2 items</h3>
                  <a>Clear all</a>
                </div>
                <div class="cart-card-nfts">
                  <div class="cart-card-nfts-image">
                    <img src="resources/image (2).png" alt="NFT">
                  </div>
                  <div class="cart-card-nfts-content">
                    <div class="cart-card-nfts-authors">
                      <p>Author</p>
                      <p>Grada</p>
                    </div>
                    <p>0.001 ETH</p>
                  </div>
                </div>
                <button class="cart-card-confirm-button">Complete Purchase</button>
              </div>
            </li>
            <li class="dropdown">
              <a id="dropdownToggleLang"><i class="fas fa-globe"></i></a>
              <div class="dropdown-content-lang">
                <a data-btn="ru">
                  <img src="resources/russia.svg" class="language-images" alt="Russian">
                  Русский
                </a>
                <a data-btn="en">
                  <img src="resources/en.svg" class="language-images" alt="English">
                  English
                </a>
                <a data-btn="kz">
                  <img src="resources/kazakh.png" class="language-images" alt="Kazakh">
                  Қазақ
                </a>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
  methods: {
    // Add methods if needed for dropdowns, calculator functionality, etc.
  }
}
</script>

<style scoped>
body {
    margin: 0;
    padding: 0;
    background: url(''); 
    background-repeat: no-repeat; 
    background-size: cover; 
    height: 100vh;
    background-color: rgb(0, 1, 21);
    font-family: 'Poppins', sans-serif;
}

nav {
    background-color: rgba(7, 0, 34, 1);
}

nav a {
    color: white;
    text-decoration: none;
}

.navbar-container {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 8vh;
}

.navbar-brand {
    width: 33%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}

.navbar-brand-logo {
    height: 8vh;
}

.navbar-brand-name {
    text-decoration: none;
    color: white;
    font-weight: bold;
    font-size: 3vh;
}

.navbar-brand-name:hover {
    text-decoration: none;
    color: rgb(34, 34, 255);
    font-weight: bold;
    font-size: 3vh;
}

.navbar-collapse {
    width: 67%;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
}

.navbar-search {
    width: 50%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.search-box {
    display: flex;
    align-items: center;
    background: linear-gradient(90deg, rgba(255,255,255,0.3), rgba(255,255,255,0.1));
    border-radius: 10px;
    height: 100%;
    padding: 1vh;
    gap: 1vh;
}

.search-box input[type="text"] {
    border: none;
    outline: none;
    height: 3vh;
    background-color: transparent;
    font-size: 2vh;
    color: white;
}

.search-box input::placeholder {
    color: rgb(255, 255, 255);
    font-size: 2vh;
}

.search-box .fa-search {
    font-size: 3vh;
    color: #ccc;
}

.navbar-items {
    width: 50%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    color: white;
}

.navbar-items ul {
    list-style-type: none;
    display: flex;
    flex-direction: row;
    gap: 3vh;
    font-size: 2vh;
}

.navbar-items ul li{
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    z-index: 10;
    width: 4.5vh;
    height: 4.5vh;
    border-radius: 5px;
    background: linear-gradient(90deg, rgba(255,255,255,0.3), rgba(255,255,255,0.1));
}

.dropdown-content-profile {
    padding: 1vh 0;
    display: none;
    position: absolute; 
    left: 0; 
    top: 100%; 
    margin-top: 2vh;
    border-radius: 10px;
    background: linear-gradient(90deg, rgba(255, 255, 255, 0.4), rgba(255, 255, 255, 0.2));
    backdrop-filter: blur(2px);
    min-width: 15vw;
    z-index: 1;
}

.dropdown-content-profile a {
    color: rgb(255, 255, 255);
    font-weight: bold;
    font-size: 3vh;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
    padding: 1vh 2vh;
}

.dropdown-content-profile a i {
    width: 2vw;
}

.dropdown-content-profile a:hover {
    background-color: rgba(0, 0, 0,0.5);
}


.dropdown-content-lang {
    padding: 1vh 0;
    display: none;
    position: absolute; 
    left: -600%; 
    top: 100%; 
    margin-top: 2vh;
    border-radius: 10px;
    background: linear-gradient(90deg, rgba(255, 255, 255, 0.4), rgba(255, 255, 255, 0.2));
    backdrop-filter: blur(2px);
    min-width: 15vw;
    z-index: 1;
}

.dropdown-content-lang a {
    color: rgb(255, 255, 255);
    font-weight: bold;
    font-size: 3vh;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
    padding: 1vh 2vh;
}

.dropdown-content-lang a i {
    width: 2vw;
}

.dropdown-content-lang a:hover {
    background-color: rgba(0, 0, 0,0.5);
}

.dropdown-content-lang a .language-images {
    width: 1.2vw;
    margin-right: 1vw;
}

.dropdown-content-cart {
    display: none;
    position: absolute; 
    left: -700%; 
    top: 100%; 
    margin-top: 2vh;
    border-radius: 20px;
    background: linear-gradient(90deg, rgba(255,255,255,0.4), rgba(255,255,255,0.2));
    backdrop-filter: blur(2px);
    min-width: 17vw;
    z-index: 1;
    padding-bottom: 1vh;
}

.cart-card-header {
    border-bottom: 1px solid white;
}

.cart-card-header, .cart-card-items {
    margin: 1vh 2vw;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
}


.cart-card-header a, .cart-card-items a {
    cursor: pointer;
}

.cart-card-items {
    margin-top: 2vh;
    height: 4vh;
}

.cart-card-nfts {
    padding: 1vh 2vw;
    margin: 2vh 0;
    display: flex;
    flex-direction: row;
    align-items: center;
}

.cart-card-nfts-image{
    height: 60px;
    padding: 0;
}

.cart-card-nfts-image img {
    height: 60px;
    padding: 0;
}

.cart-card-nfts-content {
    height: 60px;
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}

.cart-card-nfts-authors {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    margin: 0;
    padding: 0 10px;
    height: 60px;
}

.cart-card-nfts-authors p{
    line-height: 15px;
    margin: 0;
    padding: 0;
}

.cart-card-nfts:hover {
    background-color: rgba(0, 0, 0,0.5);
}

.cart-card-confirm-button {
    margin: 1vh 1vw;
    width: 250px;
    padding: 5px;
    margin-bottom: 10px;
    background-color: #0059ff;
    outline: none;
    border: none;
    color: white;
    font-size: 15px;
    border-radius: 10px;
    font-family: 'Nunito', sans-serif;
    box-sizing: border-box;
}

.dropdown-content-calculator {
    display: none;
    position: absolute; 
    left: -700%; 
    top: 100%; 
    margin-top: 2vh;
    border-radius: 20px;
    background: linear-gradient(90deg, rgba(255,255,255,0.4), rgba(255,255,255,0.2));
    backdrop-filter: blur(2px);
    min-width: 17vw;
    z-index: 1;
}

.calculator-container {
    padding: 20px;
}

.calculator-inputs {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 3px;
    gap: 5px;
}

.calculator-inputs select {
    font-size: 14px;
    background: none;
    color: white;
    border: none;
    outline: none;
}

input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

.calculator-container input{
    outline: none;
    border: none;
    border-radius: 15px;
    background: rgba(0, 0, 0, 0.4);
    width: 150px;
    font-size: 14px;
    padding: 5px 10px;
    color: white;
}

/* Profile */

.profile-container {
    padding: 10vw 20vh;
}

.profile-information {
    border-top: 1px solid transparent;
    border-image: linear-gradient(90deg, rgb(78, 78, 78), rgba(255,255,255));
    width: 100%;
    height: 30vh;
    background: linear-gradient(90deg, rgb(158, 158, 158), rgba(255,255,255,0.3));
    position: relative;
}

.profile-information img {
    position: absolute;
    top: 0;
    left: 50%;
    width: 20vw;
    border-radius: 50%;
    background: linear-gradient(to bottom,rgba(255, 255, 255, 0.3) 50%,rgba(255, 255, 255, 0) 50%);
    border: 1px solid white;
    transform: translate(-50%, -50%)
}

/* NFT Information */

.nft-container {
    padding: 10vh 10vw;
    display: flex;
    flex-direction: column;
}

.nft-information {
    width: 100%;
    background:linear-gradient(90deg, rgba(255, 255, 255, 0.3), rgba(255,255,255,0.1));
    padding: 2vw;
    position: relative;
    display: flex;
    flex-direction: row;
    gap: 3vw;
    border-radius: 1vw;
}

.nft-image {
    font-size: 1.1vw;
    text-align: center;
    color: white;
}

.nft-image img{
    width: 25vw;
    box-shadow: -1px 2px 88px -23px rgba(0,9,185,0.8);
}

.nft-information-container {
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 25vw;
}

.nft-information-container p{
    font-size: 1.2vw;
}

.nft-information-container h1{
    font-size: 2vw;
}

.nft-information-button {
    display: flex;
    gap: 1vw;
}

.nft-information-button button{
    color: white;
    outline: none;
    border: none;
    background:linear-gradient(225deg,#00E0FF, #671AE4);
    border-radius: 1vw;
    font-size: 1vw;
    
}

.border-oyu {
    width: 10vw;
    height: 10vw;
    position: absolute;
    top: 100%;
    left: 100%;
    transform: translate(-85%,-85%);
}

.buy-button {
    padding: 2vh 6vw;
}

.add-to-cart-button, .like-button {
    padding: 2vh;
}



footer {
    background-color: #333;
    color: #fff;
    font-family: 'Nunito', sans-serif;
    text-align: center;
    padding: 20px 0;
}

.footer-content {
    font-size: 20px;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
}

.footer-social-media-links ul{
    display: flex;
    padding: 0 10px;
    list-style: none;
    gap: 2vw;
    color: #fff;
}

.footer-social-media-links ul li a {
    text-decoration: none;
    color: white;
}

.footer-social-media-links ul li a:hover {
    color: rgb(0, 4, 255);
}
</style>
