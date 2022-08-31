<template>
  <link
    href="https://fonts.googleapis.com/css?family=Poppins"
    rel="stylesheet"
  />

  <div class="grid-container">
    <div class="header">
      <div class="header-title">
        <h1>DANIIL PROKOFYEV</h1>
        <h4>HBO - Software engineer</h4>
      </div>
    </div>
    <div class="portfolio-image">
      <div class="flip-card">
        <div class="flip-card-inner">
          <div class="flip-card-front">
            <img src="./../assets/profile.png" alt="profile image" />
          </div>
          <div class="flip-card-back">
            <p>Open for web dev position</p>
            <p>Vue JS</p>
          </div>
        </div>
      </div>
    </div>
    <div class="skills">
      <h2>SKILLS</h2>
      <p class="skills-list">
        Angular <br />
        Vue JS <br />
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

      <h2>EDUCATION</h2>
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
        Created an application for tracking energy in a residential area called
        Aardehuizen, Netherlands. <br />
        Angular, NodeJS, MongoDB, REST API, Highcharts
      </p>
      <div class="blue-line"></div>

      <h4 class="sub-h4">
        Signify | September 2019 - February 2020 | 5 months <br />
      </h4>
      <p class="main-content-text">
        Mendix and OutSystems low code platforms research. Internship where two
        identical web apps were created using these platforms.
      </p>
      <div class="blue-line"></div>

      <h4 class="sub-h4">
        Saxion | September 2018 - February 2019 | 5 months </h4>
      <p class="main-content-text">
        <a
        href="http://biodiversity-footprint.herokuapp.com/#/calculator"
        target="_blank"
      >Biodiversity footprint calculator</a> created on Angular for Plansup.
      </p>
      
      <div class="red-line"></div>

      <h2>HOBBIES</h2>

       <h4 class="sub-h4">
        Current project with friends | Dungeon and Dragons app
      </h4>

      <p class="main-content-text">
        Vue JS developer <br>
        <a href="https://dnd-kz-ua-ru.netlify.app/" target="_blank">
          Dungeon and Dragons
        </a>
        is an RPG board game. This is an opensource project created to improve
        web dev skills. Team of students are going to create a management tool
        where a game master and players could keep track of game statistics.
      </p>
      <br />
      <h4 class="sub-h4">Gimbarr, Chess, music, Snowboarding, Yoga</h4>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";
import { CSSPlugin } from "gsap/CSSPlugin";

gsap.registerPlugin(CSSPlugin);

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
/* #parent{
   overflow:hidden;
} */

.grid-container > div {
  padding: 0px 40px;
}

.header {
  grid-area: header;
  background-color: #ff2527;
  color: #fdfdfd;
  /* min-height: 270px; */
}

.header > div > h4 {
  color: #263547;
}

.skills > h2,
.main-content > h2,
.personal-info > h2,
.experience > h2 {
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
  border-bottom: 5px solid #4375fd;
  width: 75%;
}

.portfolio-image {
  padding-right: 0;
  display: flex;
  justify-content: center;
  background-color: #ff2527;
  grid-area: profile-image;
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
  grid-template-areas:
    "header header portfolio-image"
    "skills main main"
    "personal-info experience experience";

  padding: 10px;

  font-family: "Poppins";
  font-size: 22px;
}

@media only screen and (max-width: 900px) {
  .grid-container {
    display: flex;
    flex-wrap: wrap;

    padding: 10px;
    font-family: "Poppins";
    font-size: 22px;
  }
  div {
    width: 100%;
  }
  .header,
  .skills,
  .personal-info {
    text-align: center;
  }
}
/* .grid-container {
  display: grid;
  grid-template-areas:
    "header header header header header portfolio-image"
    "skills skills main main main main"
    "personal-info personal-info experience experience experience experience";

  padding: 10px;
} */

.sub-h3 {
  font-size: 1.5rem;
  padding-left: 1.3rem;
}

.sub-h4 {
  font-size: 1.3rem;
  padding-left: 1.3rem;
}

img {
  border-radius: 50%;
  width: 250px;
  height: 250px;
  object-fit: cover;
}

/* flip image css START*/
.flip-card {
  background-color: transparent;
  width: 250px;
  height: 250px;
  perspective: 1000px; /* Remove this if you don't want the 3D effect */
}

/* This container is needed to position the front and back side */
.flip-card-inner {
  /* position: relative; */
  width: 100%;
  height: 100%;
  text-align: center;
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
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
}

/* Style the back side */
.flip-card-back {
  background-color: #263547;
  color: white;
  font-size: 1.6rem;
  transform: rotateY(180deg);
}

/* text inside fliped card */
.flip-card-back > p:first-child {
  padding-top: 60px;
}
</style>

