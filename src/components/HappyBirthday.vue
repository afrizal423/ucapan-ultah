<template>
  <div class="container">
    <div class="one">
      <h1 class="one">
        Hiii
        <span id="name"></span>
      </h1>
      <p class="two" id="greetingText">I really like your name btw!</p>
    </div>

    <div class="three">
      <p>It's your birthday!! :D</p>
    </div>

    <div class="four">
      <div class="text-box">
        <p class="hbd-chatbox">
          Hiiii, happy birthday!!
          Wow, it's been 22 years, keep the spirit in living this life. Don't forget to keep on praying, okay?
          Wish you good health and all your wishes come true. Don't forget to be happy.
        </p>
        <p class="fake-btn">Send</p>
      </div>
    </div>

    <div class="five">
      <p class="idea-1">That's what I was going to do.</p>
      <p class="idea-2">But then I stopped.</p>
      <p class="idea-3">
        I realised, I wanted to do something<br>
        <strong>special</strong>
        .
      </p>
      <p class="idea-4">Because,</p>
      <p class="idea-5">
        You are Special
        <span>:)</span>
      </p>
      <p class="idea-6">
        <span>S</span>
        <span>O</span>
      </p>
    </div>

    <div class="six">
      <img src="/img/irene.jpg" alt="profile" class="profile-picture" id="imagePath"/>
      <img src="img/hat.svg" alt="hat" class="hat" />
      <div class="wish">
        <h3 class="wish-hbd">Happy Birthday!</h3>
        <h5 id="wishText">May the js.prototypes always be with you! ;)</h5>
      </div>
    </div>

    <div class="seven">
      <div class="baloons">
        <img src="img/ballon2.svg" alt="" />
        <img src="img/ballon1.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
        <img src="img/ballon1.svg" alt="" />
        <img src="img/ballon2.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
        <img src="img/ballon2.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
        <img src="img/ballon1.svg" alt="" />
        <img src="img/ballon2.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
        <img src="img/ballon2.svg" alt="" />
        <img src="img/ballon1.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
        <img src="img/ballon2.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
        <img src="img/ballon1.svg" alt="" />
        <img src="img/ballon2.svg" alt="" />
        <img src="img/ballon1.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
        <img src="img/ballon1.svg" alt="" />
        <img src="img/ballon2.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
        <img src="img/ballon2.svg" alt="" />
        <img src="img/ballon1.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
        <img src="img/ballon2.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
        <img src="img/ballon1.svg" alt="" />
        <img src="img/ballon2.svg" alt="" />
        <img src="img/ballon1.svg" alt="" />
        <img src="img/ballon3.svg" alt="" />
      </div>
    </div>

    <div class="eight">
      <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="20" />
      </svg>
      <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="20" />
      </svg>
      <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="20" />
      </svg>
      <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="20" />
      </svg>
      <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="20" />
      </svg>
      <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="20" />
      </svg>
      <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="20" />
      </svg>
      <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="20" />
      </svg>
      <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="20" />
      </svg>
    </div>

    <div class="nine">
      <p>Okay, now come back and tell me if you liked it.</p>
      <p @click="restart">Or click, if you want to watch it again.</p>
      <p class="last-smile">:)</p>
    </div>
  </div>
</template>

<script>
  import Swal from 'sweetalert2'
  import { gsap, Expo, Elastic } from 'gsap';
  import { CSSPlugin } from 'gsap/CSSPlugin'
  gsap.registerPlugin(CSSPlugin);

  const myCards = [
    {
      id: 0,
      name: 'Prima carta',
    },
    {
      id: 1,
      name: 'Seconda carta',
    },
    {
      id: 2,
      name: 'Terza carta',
    },
    {
      id: 3,
      name: 'Quarta carta',
    }
  ];

  const ideaTextTrans = {
    opacity: 0,
    y: -20,
    rotationX: 5,
    skewX: "15deg"
  }

  const ideaTextTransLeave = {
    opacity: 0,
    y: 20,
    rotationY: 5,
    skewX: "-15deg"
  }

  const tl = gsap.timeline();
  const audio = new Audio('/music/hbd.mpeg'); 

  export default {
    name: 'HappyBirthday',
    data() {
      return {
        cards: myCards,
      };
    },
    methods: {
      pertama(){
        Swal.fire({
        title: 'Do you want to play music in the background?',
        icon: 'warning',
        showCancelButton: true,
        confirmButtonColor: '#3085d6',
        cancelButtonColor: '#d33',
        confirmButtonText: 'Yes',
        cancelButtonText: 'No',
      }).then((result) => {
        if (result.isConfirmed) {          
          audio.volume = 0.185;
          audio.play();
          this.ambildata();
          this.jalanin();
        } else {
          this.ambildata();
          audio.pause();
          audio.currentTime = 0;
          this.jalanin();
        }
      });
      },
      ambildata(){
        fetch("customize.json")
        .then(data => data.json())
        .then(data => {
          Object.keys(data).map(customData => {
            if (data[customData] !== "") {
              if (customData === "imagePath") {
                document
                  .getElementById(customData)
                  .setAttribute("src", data[customData]);
              } else {
                document.getElementById(customData).innerText = data[customData];
              }
            }
          });
        });
      },
      jalanin(){
      const textBoxChars = document.getElementsByClassName("hbd-chatbox")[0];
      const hbd = document.getElementsByClassName("wish-hbd")[0];

      textBoxChars.innerHTML = `<span>${textBoxChars.innerHTML
        .split("")
        .join("</span><span>")}</span`;

      hbd.innerHTML = `<span>${hbd.innerHTML
        .split("")
        .join("</span><span>")}</span`;     

      tl.to(".container", 0.6, {
        visibility: "visible"
      })
        .from(".one", 0.7, {
          opacity: 0,
          y: 10
        })
        .from(".two", 0.4, {
          opacity: 0,
          y: 10
        })
        .to(".one",
          0.7,
          {
            opacity: 0,
            y: 10
          },
        "+=3.5")
        .to(".two",
          0.7,
          {
            opacity: 0,
            y: 10
          },
        "-=1")
        .from(".three", 0.7, {
          opacity: 0,
          y: 10
        })
        .to(".three",
          0.7,
          {
            opacity: 0,
            y: 10
          },
        "+=3")
        .from(".four", 0.7, {
          scale: 0.2,
          opacity: 0,
        })
        .from(".fake-btn", 0.3, {
          scale: 0.2,
          opacity: 0,
        })
        .staggerTo(
          ".hbd-chatbox span",
          1.5, {
            visibility: "visible",
          },
          0.05
        )
        .to(".fake-btn", 0.1, {
          backgroundColor: "rgb(127, 206, 248)",
        },
        "+=4")
        .to(
          ".four",
          0.5, {
            scale: 0.2,
            opacity: 0,
            y: -150
          },
        "+=1")
        .from(".idea-1", 0.7, ideaTextTrans)
        .to(".idea-1", 0.7, ideaTextTransLeave, "+=2.5")
        .from(".idea-2", 0.7, ideaTextTrans)
        .to(".idea-2", 0.7, ideaTextTransLeave, "+=2.5")
        .from(".idea-3", 0.7, ideaTextTrans)
        .to(".idea-3 strong", 0.5, {
          scale: 1.2,
          x: 10,
          backgroundColor: "rgb(21, 161, 237)",
          color: "#fff",
        })
        .to(".idea-3", 0.7, ideaTextTransLeave, "+=2.5")
        .from(".idea-4", 0.7, ideaTextTrans)
        .to(".idea-4", 0.7, ideaTextTransLeave, "+=2.5")
        .from(
          ".idea-5",
          0.7, {
            rotationX: 15,
            rotationZ: -10,
            skewY: "-5deg",
            y: 50,
            z: 10,
            opacity: 0,
          },
          "+=1.5"
        )
        .to(
          ".idea-5 span",
          0.7, {
            rotation: 90,
            x: 8,
          },
          "+=1.4"
        )
        .to(
          ".idea-5",
          0.7, {
            scale: 0.2,
            opacity: 0,
          },
          "+=2"
        )
        .staggerFrom(
          ".idea-6 span",
          0.8, {
            scale: 3,
            opacity: 0,
            rotation: 15,
            ease: Expo.easeOut,
          },
          0.2
        )
        .staggerTo(
          ".idea-6 span",
          0.8, {
            scale: 3,
            opacity: 0,
            rotation: -15,
            ease: Expo.easeOut,
          },
          0.2,
          "+=1.5"
        )
        .staggerFromTo(
          ".baloons img",
          2.5, {
            opacity: 0.9,
            y: 1400,
          }, {
            opacity: 1,
            y: -1000,
          },
          0.2
        )
        .from(
          ".profile-picture",
          0.5, {
            scale: 3.5,
            opacity: 0,
            x: 25,
            y: -25,
            rotationZ: -45,
          },
          "-=2"
        )
        .from(".hat", 0.5, {
          x: -100,
          y: 350,
          rotation: -180,
          opacity: 0,
        })
        .staggerFrom(
          ".wish-hbd span",
          0.7, {
            opacity: 0,
            y: -50,
            // scale: 0.3,
            rotation: 150,
            skewX: "30deg",
            ease: Elastic.easeOut.config(1, 0.5),
          },
          0.1
        )
        .staggerFromTo(
          ".wish-hbd span",
          0.7, {
            scale: 1.4,
            rotationY: 150,
          }, {
            scale: 1,
            rotationY: 0,
            color: "#ff69b4",
            ease: Expo.easeOut,
          },
          0.1,
          "party"
        )
        .from(
          ".wish h5",
          0.5, {
            opacity: 0,
            y: 10,
            skewX: "-15deg",
          },
          "party"
        )
        .staggerTo(
          ".eight svg",
          1.5, {
            visibility: "visible",
            opacity: 0,
            scale: 80,
            repeat: 3,
            repeatDelay: 1.4,
          },
          0.3
        )
        .to(".six", 0.5, {
          opacity: 0,
          y: 30,
          zIndex: "-1",
        })
        .staggerFrom(".nine p", 1, ideaTextTrans, 1.2)
        .to(
          ".last-smile",
          0.5, {
            rotation: 90,
          },
          "+=1"
        );
      },
      restart(){
        tl.restart();
      }
    },
    mounted() {
      this.pertama()
    },
  }
</script>
<style scoped>

</style>