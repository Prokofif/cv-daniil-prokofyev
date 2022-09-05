<template>
  <link
    href="https://fonts.googleapis.com/css?family=Poppins"
    rel="stylesheet"
  />

  <div class="grid-container">
    <div class="header">
      <div class="header-title">
        <h1>DANIIL PROKOFYEV</h1>
        <h4>
          <a
            class="typewrite"
            data-period="2000"
            data-type='[ "Hi, Im ", "I am Creative.", "I Love Design.", "I Love to Develop." ]'
          >
            <span class="wrap"></span>
          </a>
        </h4>
      </div>
    </div>
    <div class="portfolio-image">
      <div class="flip-card">
        <div class="flip-card-inner">
          <div class="flip-card-front">
            <img src="./../assets/profile.png" alt="profile image" />
          </div>
          <div class="flip-card-back">
            <p>Open for a web dev position</p>
          </div>
        </div>
      </div>
    </div>
    <div class="skills">
      <h2>SKILLS</h2>
      <p class="skills-list">
        Angular <br />
        Vue JS, Vuex <br />
        PHP<br />
        Python (Machine learning)<br />
        OutSystems & Mendix<br />
        C# (Unity, VS)<br />
        Java (Android Studio)<br />
        <br />

        MongoDB, MySQL <br />
        RestAPI<br />
        Git, SCRUM<br />
        Professional communication<br />
        Presentation<br />
      </p>
    </div>

    <div class="personal-info">
      <h2>PERSONAL INFO</h2>
      <p class="personal-info-content">
        Tel: +31 6 38 41 14 86 <br />
        Mail: prokofev.danil22@gmail.com<br /><br />

        Date of birth: 23.05.1998<br />
        Place of birth: Russia<br />
        <br />
        City: Enschede<br />
        Country: Netherlands<br />
      </p>
    </div>

    <div class="main-content">
      <h2>ABOUT</h2>
      <p class="main-content-text">
        I'm a 24 y.o. software engineer with 2 years of experience. I want to
        work as a VueJS developer in a team of pros to create new quality
        products.
      </p>
      <div class="red-line"></div>

      <h2 class="education-h">EDUCATION</h2>
      <h4 class="sub-h4">
        Saxion University of Applied Science <br />
        HBO Software Engineering | 2016-2022 <br />
        Bachelor degree
      </h4>
      <div class="red-line"></div>
    </div>
    <div class="experience">
      <h2>EXPERIENCE</h2>
      <h4 class="sub-h4">TS24 B.V. | July 2020 - May 2022</h4>
      <p class="main-content-text">
        Full stack PHP web developer responsible for solving issues and
        implementing features to improve an internet shop.
      </p>
      <div class="blue-line"></div>

      <h4 class="sub-h4">Saxion Graduation Project | Sep 2021 - April 2022</h4>
      <p class="main-content-text">
        Information gathering, Interview final users, Design, Build, Test and Launch an application from scratch for tracking energy in a residential area called
       Aardehuizen, Netherlands. <br />
      </p>
      <p class="main-content-text">
        Angular - frontend <br> NodeJS - backend <br> MongoDB - online database <br> Highcharts - charts library <br>  REST API - charts data
      </p>
      <div class="blue-line"></div>

      <h4 class="sub-h4">
        Signify | September 2019 - February 2020 | 5 months <br />
      </h4>
      <p class="main-content-text">
        Mendix and OutSystems low code platforms research. Internship where two
        identical web apps were created using these platforms.  Each app is made
        of: <br>
      </p>
        <p class="main-content-text span-gap" style="margin:0;">
        <b>Log in/Sign up</b> page with session-based authentication and authorization proccess (Logic building). <br>
        </p>
        
        <p class="main-content-text span-gap" style="margin:0;">
        <b>Modal</b> with dropdowns to select specific data (Logic building). <br>
        </p>

        <p class="main-content-text span-gap" style="margin:0;">
        <b>Main</b> page with a multiple line graph, bar charts (REST API data processing) and a comment component (Database, SQL). <br>
        </p>
        <p class="main-content-text span-gap" style="margin-top:0;">
        <b>About</b> page where user details can be edited (Data binding).<br>
        </p>
      <div class="blue-line"></div>

      <h4 class="sub-h4">Saxion web dev project | September 2018 - February 2019 | 5 months</h4>
      <p class="main-content-text">
        <a
          href="http://biodiversity-footprint.herokuapp.com/#/calculator"
          target="_blank"
          >Biodiversity footprint calculator</a
        > - web application created in a team of 4 students on Angular for Plansup. 
      </p>
      <div class="blue-line"></div>

      <h4 class="sub-h4">Saxion Android Studio project | September 2017 - February 2018 | 5 months</h4>
      <p class="main-content-text">
        Team of 5 students created a Fishing game from scratch written on Java in Android Studio.  
      </p>

      

      <div class="red-line"></div>

      <h2 class="hobbies-h">HOBBIES</h2>

      <h4 class="sub-h4">Dungeon and Dragons app on Vue JS</h4>

      <p class="main-content-text">
        <a href="https://dnd-kz-ua-ru.netlify.app/" target="_blank">
          Dungeon and Dragons
        </a>
        is an open source project created with friends to improve our skills.
        <br />
        DnD is a role-play board game. We want create a management tool and add
        our own features to make it even more fun!
      </p>
      <br />
      <h4 class="sub-h4">Gimbarr, Chess, Music, Snowboarding, Yoga</h4>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";
import { CSSPlugin } from "gsap/CSSPlugin";

gsap.registerPlugin(CSSPlugin);


//todo
function delay(milliseconds){
    return new Promise(resolve => {
        setTimeout(resolve, milliseconds);
    });
}

async function init(){
    console.log("Executed now");
    await delay(3000);
    console.log("Executed after 3 seconds wait");

    //todo place typing text function here

    var TxtType = function (el, toRotate, period) {
    this.toRotate = toRotate;
    this.el = el;
    this.loopNum = 0;
    this.period = parseInt(period, 10) || 2000;
    this.txt = "";
    this.tick();
    this.isDeleting = false;
  };

  TxtType.prototype.tick = function () {
  var i = this.loopNum % this.toRotate.length;
  var fullTxt = this.toRotate[i];

  if (this.isDeleting) {
    this.txt = fullTxt.substring(0, this.txt.length - 1);
  } else {
    this.txt = fullTxt.substring(0, this.txt.length + 1);
  }

  this.el.innerHTML = '<span class="wrap">' + this.txt + "</span>";

  var that = this;
  var delta = 200 - Math.random() * 100;

  if (this.isDeleting) {
    delta /= 2;
  }

  if (!this.isDeleting && this.txt === fullTxt) {
    delta = this.period;
    this.isDeleting = true;
    console.log(this.txt);
  } else if (this.isDeleting && this.txt === "") {
    this.isDeleting = false;
    this.loopNum++;
    delta = 500;
    console.log(this.txt);
  }
  if (this.txt === "I Love to Develop.") {
      var css = document.createElement("style");
      css.type = "text/css";
      css.innerHTML = ".typewrite > .wrap { border-right: 0em}";
      document.body.appendChild(css); 
    return 0;
  }

  setTimeout(function () {
    that.tick();
  }, delta);
};

  var elements = document.getElementsByClassName("typewrite");
  for (var i = 0; i < elements.length; i++) {
    var toRotate = elements[i].getAttribute("data-type");
    var period = elements[i].getAttribute("data-period");
    if (toRotate) {
      new TxtType(elements[i], JSON.parse(toRotate), period);
    }
  }
  // INJECT CSS
  var css = document.createElement("style");
  css.type = "text/css";
  css.innerHTML = ".typewrite > .wrap { border-right: 0.08em solid #fff}";
  document.body.appendChild(css); 
}

init();

// start of header text animation





// end of header text animation

export default {
  name: "HelloWorld",

  //todo apply. not used
  methods: {
    simpleFade(i) {
      gsap.fromTo(
        this.$refs.cards[i],
        {
          autoAlpha: 1,
        },
        {
          autoAlpha: 0,
          duration: 0.35,
        }
      );
      this.fadeIn();
    },
    fadeIn() {
      document.getElementById("box1").style.visibility = "visible";
      gsap.fromTo(
        ".box1",
        { x: 0, y: 0, autoAlpha: 0 },
        { x: 0, y: 50, autoAlpha: 1, duration: 1 }
      );
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


.header {
  grid-area: header;
  background-color: #ff2527;
  color: #fdfdfd;
  min-height: 187px;
}

.header > div > h4 {
  color: #263547;
}

.header,
.skills,
.main-content,
.personal-info,
.experience {
  padding: 0 40px;
}

.skills > h2,
.main-content > h2,
.personal-info > h2,
.experience > h2 {
  text-transform: uppercase;
  font-size: 1.5rem;
}

.skills,
.personal-info {
  grid-area: skills;
  background-color: #263547;
  color: #fd4345;
}
.skills-list,
.personal-info-content {
  font-size: 1.2rem;
  color: #fdfdfd;
  padding-bottom: 20px;
}



.education-h {
  padding-top: 10px;
}
.hobbies-h {
  padding-top: 40px;
}

.main-content,
.experience {
  grid-area: main;
  background-color: #ffffff;
  color: #263547;
}

.main-content-text {
  font-size: 1.2rem;
  padding-left: 1.3rem;
}

.red-line {
  border-bottom: 5px solid #fd4345;
}

.blue-line {
  border-bottom: 5px solid #0044ff;
  width: 75%;
  margin-bottom: 50px;
}
a:visited{
  color:#1856ff;
}

.portfolio-image {
  display: flex;
  justify-content: center;
  background-color: #ff2527;
  grid-area: portfolio-image;
  grid-column: 3;
  grid-row: 1;
}

.personal-info {
  grid-area: personal-info;
}
.experience {
  grid-area: experience;
  padding-top: 0px;
  margin-top: 0px;
}

.grid-container {
  display: grid;
  grid-template-columns: auto auto 200px;
  grid-template-areas:
    "header header portfolio-image"
    "skills main main"
    "personal-info experience experience";

  padding: 10px;

  font-family: "Poppins";
  font-size: 22px;
}

.sub-h4 {
  font-size: 1.3rem;
  padding-left: 1.3rem;
}

img {
  border-radius: 50%;
  width: 150px;
  height: 150px;
  object-fit: cover;
}

/* flip image css START*/
.flip-card {
  background-color: transparent;
  width: 170px;
  height: 170px;
  perspective: 1000px; /* Remove this if you don't want the 3D effect */
}

/* This container is needed to position the front and back side */
.flip-card-inner {
  width: 100%;
  height: 100%;
  text-align: center;
  padding: 10px 0;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

/* Do an horizontal flip when you move the mouse over the flip box container */
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}
/* Position the front and back side */
.flip-card-front,
.flip-card-back {
  border-radius: 50%;

  border: 5px solid #fdfdfd;
  padding: 5px;
  position: absolute;
  width: 150px;
  height: 150px;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
}

/* Style the back side */
.flip-card-back {
  background-color: #263547;
  color: white;
  font-size: 1.1rem;
  transform: rotateY(180deg);
}

/* text inside fliped card */
.flip-card-back > p:first-child {
  padding-top: 31px;
}

/* SMALLER SCREEN */
@media only screen and (max-width: 900px) {
  .grid-container {
    display: flex;
    flex-wrap: wrap;
    padding: 10px;
    font-family: "Poppins";
    font-size: 22px;
  }
  h1 {
    font-size: 2rem;
  }

  div {
    width: 100%;
  }
  .portfolio-image {
    padding: 0 0 20px ;
  }
  .header,
  .skills,
  .personal-info {
    text-align: center;
  }
  .education-h,
  .hobbies-h {
    padding-top: 0px;
  }

}
.span-gap {
  text-indent: 2rem;
  /* margin: 0; */
}



</style>

