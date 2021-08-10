


<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Events App</title>
    
    
    
    
    
    <style>
        /* Created by 🔫 Rick Grimes */

@import url('https://fonts.googleapis.com/css2?family=Varela+Round&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Prompt:wght@500&display=swap');

body {
    margin: 0;
    padding: 0;
    overflow-x: hidden;
backgroundnya:blue;
}

#loader {
    width: 100%;
    height: 100vh;
    /*background: red;*/
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: fantasy;
}


#App {
    width: 100%;
    height: 100vh;
    position: relative;
    display: none;
}

#home-screen {
    /*display: block;*/
    width: 100%;
    height: 100vh;
    position: absolute;
    transform-origin: top left;
    transition: 0.5s;
}

#event-details-screen {
    /*display: none;*/
    width: 100%;
    height: 100vh;
    position: absolute;
    left: 100%;
    z-index: 3;
    transition: 0.5s;
}

.home-screen-header-container {
    width: 100%;
    height: 70px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.home-screen-header-container div {
    margin: 20px;
}

.header-text-container {
    font-size: 22px;
    font-weight: bold;
    font-family: 'Varela Round';
}

.events-card-container {
    width: 100%;
    height: calc(100vh - 140px);
    /*background: purple;*/
    background: white;
}

.card-data-container {
    width: 100%;
    height: 15%;
    /*background: red;*/
    display: flex;
}

.data-main-one {
    width: 70%;
    height: 100%;
    /*background: purple;*/
}

#event-name-container {
    width: 100%;
    height: 60%;
    /*background: green;*/
    font-size: 28px;
    font-family: 'Prompt';
    padding-left: 30px;
    display: flex;
    align-items: center;
}

#venue-container {
    width: 100%;
    height: 40%;
    font-size: 14px;
    padding-left: 30px;
    font-family: 'Prompt';
}

.data-main-two {
    width: 30%;
    height: 60%;
    /*background: gray;*/
    font-size: 12px;
    /*font-weight: bold;*/
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Prompt';
}

.main-card-container {
    width: 100%;
    height: 85%;
    /*background: green;*/
    position: relative;
    overflow-x: hidden;
}

.card {
    border-radius: 12px;
    position: absolute;
    transition: 0.5s;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
}

.gone {
    width: 210px;
    height: 85%;
    /*background: green;*/
    top: 7.5%;
    left: -100%;
    z-index: 1;    
}

.first {
    width: 170px;
    height: 85%;
    /*background: grey;*/
    top: 7.5%;
    left: 30px;
    z-index: 2;
}

.second {
    width: 160px;
    height: 70%;
    /*background: purple;*/
    top: 15%;
    left: 120px;
    opacity: 1;
    pointer-events: none;
}

.third {
    width: 150px;
    height: 55%;
    /*background: blue;*/
    top: 22.5%;
    left: 210px;
    z-index: 0;
    opacity: 0.3;
    pointer-events: none;
}

.coming {
    width: 150px;
    height: 55%;
    /*background: blue;*/
    top: 22.5%;
    left: 100%;
    z-index: -1;
    opacity: 0;
}

.home-screen-footer-container {
    width: 100%;
    height: 70px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: white;
}

.home-screen-footer-container div {
    margin: 20px;
}

.add-event-container {
    font-family: 'Varela Round';
}

.event-banner-container {
    width: 100%;
    height: 60vh;
    background: linear-gradient(rgba(100,100,100,0.4), rgba(100,100,100,0.4)), url(Lighthouse.jpg);
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
}

.back-btn-container {
    width: 100%;
    height: 80px;
    /*background: purple;*/
    display: flex;
}

.back-btn-container div {
    display: flex;
    align-items: center;
}

#back-btn {
    width: 15%;
    height: 100%;
    /*background: green;*/
    justify-content: center;
}

#page-name {
    /*background-color: aqua;*/
    font-size: 20px;
    color: white;
    font-family: 'Varela Round';
}

.event-details-main {
    width: 100%;
    height: calc(40vh - 10px);
    /*background: red;*/
    padding-top: 10px;
    background: white;
}

.details-event-name {
    width: 100%;
    /*background: purple;*/
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.details-event-name span {
    margin-left: 30px;
    font-size: 28px;
    font-family: 'Prompt';
}

.details-event-name button {
    margin-right: 30px;
    padding: 10px;
    border: none;
    border-radius: 2px;
    font-family: 'Varela Round';
}

.details-event-name button[data-i="yes"] {
    background: rgb(80, 200, 80);
    color: white;
}

.details-event-name button[data-i="no"] {
    background: white;
    color: black;
    border: 1px solid rgb(80, 200, 80);
}

.details-event-location {
    margin-left: 30px;
    font-size: 14px;
    font-family: 'Prompt';
}

.details-event-time {
    margin-left: 30px;
    font-size: 12px;
    font-family: 'Prompt';
}

.details-options-container {
    margin-top: 10vh;
    width: 100%;
    display: flex;
    justify-content: space-around;
}

.details-options-container button {
    border: none;
    font-family: 'Varela Round';
    font-size: 14px;
}

.details-options-container button:nth-child(2) {
    /*background: red;*/
    padding: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.details-options-container button:nth-child(2) span {
    color: rgb(80, 200, 80);
    margin-right: 10px;
}

#navigation-screen {
    width: 100%;
    height: 100vh;
    background: transparent;
    position: absolute;
    z-index: -1;
    display: flex;
    align-items: flex-end;
}

#navigation-screen nav {
    width: 150px;
    height: auto;
    display: flex;
    flex-direction: column;
}

#navigation-screen nav a {
    font-size: 18px;
    margin: 10px;
    color: black;
    font-family: 'Varela Round';
    text-decoration: none;
}
    </style>
    
    
    
    
    
    
    <script>
        
       // Created by 🔫 Rick Grimes

//variable definitions.
let homeScreen, detailsScreen;

let cardContainer;

let firstCard, secondCard, thirdCard;
let gone, coming;
let allCards;

let touchStartX = 0, touchEndX = 0;

let eventNameDiv, eventVenueDiv, eventTimeDiv;

const cardData = [
    {
        title: 'siGO', 
        venue: 'Taxi and curier', 
        date: 'more', 
        image: 'https://thumbassite.files.wordpress.com/2021/03/flyerdesign_13032021_221929.jpeg?w=650'
    },
    {
        title: 'siPAY', 
        venue: 'Billing and payment', 
        date: 'more', 
        image: 'https://thumbassite.files.wordpress.com/2021/03/flyerdesign_13032021_222628.jpeg' 
    },
    {
        title: 'siSHOP', 
        venue: 'ecomerce', 
        date: 'more', 
        image: 'https://thumbassite.files.wordpress.com/2021/03/flyerdesign_13032021_224740.jpeg'
    },
    {
        title: 'siClEAN', 
        venue: 'loundry and cleaning', 
        date: 'more', 
        image: 'https://thumbassite.files.wordpress.com/2021/03/flyerdesign_13032021_225142.jpeg'
        
    },
    {
        title: 'siNIC', 
        venue: 'service car',
        date: 'More', 
        image: 'https://thumbassite.files.wordpress.com/2021/03/flyerdesign_13032021_223548.jpeg'
    },
    {
        title: 'siHELP', 
        venue: 'help u', 
        date: 'more', 
        image: 'https://thumbassite.files.wordpress.com/2021/03/flyerdesign_13032021_224421.jpeg'
    },
];

let cardNumber = 0;

//card changer function
const changeCard = () => {

    //check which side it is swiped to
    //starting position is less than ending means right swipe
    //starting position is greater than ending means left swipe
    if (Math.round(touchStartX) < Math.round(touchEndX)) {

        // there should be atleast one element in gone array
        if (gone.length !== 0) {

            //any card should not be null otherwise it will throw error
            if (firstCard != null) {

                //first card moved to second card after swipe
                firstCard.classList.add('second');
                firstCard.classList.remove('first');
                cardNumber--;

            }

            if (secondCard != null) {

                //second card moved to third card after swipe
                secondCard.classList.add('third');
                secondCard.classList.remove('second');

            }

            if (thirdCard != null) {

                //third card moved as coming card
                thirdCard.classList.add('coming');
                thirdCard.classList.remove('third');

            }

            //get last element from gone array and make it first available card
            gone[gone.length - 1].classList.add('first');
            gone[gone.length - 1].classList.remove('gone');

        }

    } else if(Math.round(touchStartX) === Math.round(touchEndX)) {
        // console.log("equal");
        //Does nothing really, lol
    } else {

        //again, check for null
        if (secondCard != null) {

            if (firstCard != null) {

                //first card moved to gone
                firstCard.classList.add('gone');
                firstCard.classList.remove('first');
                cardNumber++;

            }

            if (secondCard != null) {

                //second becomes first
                secondCard.classList.add('first');
                secondCard.classList.remove('second');

            }

            if (thirdCard != null) {

                //third becomes second
                thirdCard.classList.add('second');
                thirdCard.classList.remove('third');

            }

            if (coming.length !== 0) {
            
                //first card from coming array becomes third
                coming[0].classList.add('third');
                coming[0].classList.remove('coming');

            }
        }

    }

    //setting variables again because classes are changed
    initializeCardVars();
    changeCardDetail(cardData[cardNumber]);

}

//initialize/re-initializing variabeles
const initializeCardVars = () => {
    gone = document.getElementsByClassName('gone');
    coming = document.getElementsByClassName('coming');
    firstCard = document.querySelector('.first');
    secondCard = document.querySelector('.second');
    thirdCard = document.querySelector('.third');
}

const cardOpener = (index) => {
    alert(index);
}

const changeCardDetail = (data) => {
    eventNameDiv.innerText = data.title;
    eventVenueDiv.innerText = data.venue;
    eventTimeDiv.innerText = data.date;
}

const openDetailsPage = (data) => {
    // homeScreen.style.display = "none";
    const eventNameSpan = document.querySelector('.details-event-name span');
    eventNameSpan.innerText = data.title;
    const eventLocation = document.querySelector('.details-event-location');
    eventLocation.innerText = data.venue;
    const eventTime = document.querySelector('.details-event-time');
    eventTime.innerText = data.date;
    const bannerContainer = document.querySelector('.event-banner-container');
    bannerContainer.style.background = `linear-gradient(rgba(100,100,100,0.4), rgba(100,100,100,0.4)), url(${data.image})`;
    bannerContainer.style.backgroundPosition = "top";
    bannerContainer.style.backgroundSize = "cover";
    bannerContainer.style.backgroundRepeat = "no-repeat";
    detailsScreen.style.left = "0";
}

let isNavOpen = false;

const openNav = () => {
    if (!isNavOpen) {
        homeScreen.style.transform = "rotateZ(-25deg)";
        cardContainer.style.pointerEvents = "none";
    } else {
        homeScreen.style.transform = "rotateZ(0deg)";
        cardContainer.style.pointerEvents = "all";
    }
    isNavOpen = !isNavOpen;
}

const backBtn = () => {
    detailsScreen.style.left = "100%";
}

//wait for window to load
window.onload = () => {

    homeScreen = document.getElementById('home-screen');
    detailsScreen = document.getElementById('event-details-screen');

    cardContainer = document.getElementById('card-container');
    eventNameDiv = document.getElementById('event-name-container');
    eventVenueDiv = document.getElementById('venue-container');
    eventTimeDiv = document.getElementById('time-container');

    cardData.forEach((data, index) => {

        let classes = "card ";
        switch(index) {
            case 0: 
                classes += "first";
                changeCardDetail(data);
                break;
            case 1:
                classes += "second";
                break;
            case 2: 
                classes += "third";
                break;
            default:
                classes += "coming";
                break;
        }
        const cardDiv = document.createElement('div');
        cardDiv.classList = classes;
        cardDiv.style.backgroundImage = `url(${data.image})`;
        cardDiv.addEventListener('click', () => openDetailsPage(data));
        cardContainer.appendChild(cardDiv);

    });

    //select from DOM
    cardChangeDetector = document.getElementById('change-detector');
    allCards = document.querySelectorAll('.card');
    // allCards.forEach((card, index) => {
    //     card.addEventListener('click', () => {
    //         cardOpener(index);
    //     });
    // });

    //for setting initial values to variable.
    initializeCardVars();

    //mousedown and mouseup are for desktop browsers
    cardContainer.addEventListener('mousedown', (e) => {
        // console.log(e.clientX);
        touchStartX = e.clientX;
    });
    
    cardContainer.addEventListener('mouseup', (e) => {
        // console.log(e.clientX);
        touchEndX = e.clientX;
        changeCard();
    });


    //touchstart and touchend events are for mobiles
    cardContainer.addEventListener('touchstart', (e) => {
        // console.log(e.clientX);
        // alert("started");
        touchStartX = e.touches[0].clientX;
    });
    
    cardContainer.addEventListener('touchend', (e) => {
        // console.log(e.clientX);
        // alert("ended");
        touchEndX = e.changedTouches[0].clientX;
        changeCard();
    });

    const loader = document.querySelector('#loader');
    const app = document.querySelector('#App');
    loader.style.display = "none";
    app.style.display = "block";

}
    </script>
    
    
    
</head>
<body>

    <div id="loader">Loading...</div>

    <div id="App">
        
        <div id="home-screen">
            
            <div class="home-screen-header-container">
                <div class="header-text-container">
                  member
                </div>
                <div class="search-bar-container">
                   <a href=''><img src="https://dl.dropbox.com/s/zkpyvjxtctqio6a/search.svg?dl=0" alt="search bar"></a>
                </div>
            </div>

            <div class="events-card-container">
                <div class="card-data-container">
                    <div class="data-main-one">
                        
                        <div id="event-name-container">Fashion Talk</div>
                        <div id="venue-container">Rajkot, India</div>

                    </div>
                    <div class="data-main-two">

                        <div id="time-container">Nov 14, 2020</div>

                    </div>
                </div>
                <div class="main-card-container" id="card-container">
                </div>
            </div>

            <div class="home-screen-footer-container">
                <div class="menu-btn-container">
                    <img src="https://dl.dropbox.com/s/lf253sp8pctzs3h/menu%281%29.svg?dl=0" alt="menu button" onclick="openNav()">
                </div>
                <div class="add-event-container">
 <a href="http://cipsonchat.blogspot.com
">Help?</a>


</div>
            </div>

        </div>

        <div id="event-details-screen">
            
            <div class="event-banner-container">
        
                <div class="back-btn-container">
                    
                    <div id="back-btn" onclick="backBtn()">
                        
                        <img src="https://dl.dropbox.com/s/jpnk5cs7qveiwbm/left-arrow%281%29.svg?dl=0" alt="back button">

                    </div>
                    <div id="page-name">service</div>

                </div>

            </div>

            <div class="event-details-main">
                        
                <div class="details-event-name">
                    <span></span>
                    <button data-i="no">Interested</button>
                </div>
                <div class="details-event-location"></div>
                <div class="details-event-time"></div>

                <div class="details-options-container">
                    
                    <button>

<a href="https://www.surveymonkey.com/r/DG2BRX5"
>Driver</a> 

 


</button>
                    <button>
                        <span>




<a href="https://jgjk.mobi/p/604d5ddd9f866
" style="text-decoration:none">Member</a> 

 


</span>
                 

       <img src="https://dl.dropbox.com/s/a91u0mrgctrmye3/right-arrow.svg?dl=0" style="transform: rotateZ(180deg)">
                    </button>

                </div>

            </div>

        </div>

        <div id="navigation-screen">
            
            <nav>
                <a href="#">Home</a>
                <a href="#">Pathner</a>
                <a href="#">carier</a>
                <a href="#">Contact Us</a>
            </nav>

        </div>

    </div>


    <script src="script.js"></script>
</body>
</html>
