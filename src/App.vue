<template>
    <div class="msg">Happy New Year</div>

    <div class="year">
        <span class="first_year">
            <span class="y1">2</span>
            <span class="y2">0</span>
            <span class="y3">2</span>
        </span>
        <span class="old">3</span>
        <span class="y4 new">4</span>
        <div class="balloon"></div>
    </div>
    <div class="firework" id="firework1">
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
    </div>
    <div class="firework" id="firework2">
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
    </div>
    <div class="firework" id="firework3">
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
        <div class="cracker"></div>
    </div>
</template>

<script>

export default {
    name: "App",
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Bilbo+Swash+Caps&family=Montserrat:wght@100&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@100&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300&display=swap");

*,
*:after,
*:before {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    transition: all 100ms ease-in;
    -webkit-transition: all 100ms ease-in;
}
#app {
	display: block;
	width: 100vw;
    height: 100vh;
}

body {
    background: #000;
    overflow: hidden;
    height: 100vh;
}
.msg {
    width: 100%;
    font-family: "Bilbo Swash Caps", cursive;
    font-size: 100px;
    font-weight: bolder;
    color: red;
    text-align: center;
    position: absolute;
    top: 50%;
    opacity: 0;
    animation: message 2s ease-in-out 6s forwards;
}

@keyframes message {
    0% {
        opacity: 0;
        margin-top: 0;
    }
    100% {
        opacity: 1;
        margin-top: -200px;
    }
}
.y1 {
    color: #fff;
    animation: y1colorful 2s ease-in-out 5.75s forwards;
}
.y2 {
    color: #fff;
    animation: y2colorful 25 ease-in-out 5.75s forwards;
}
.y3 {
    color: #fff;
    animation: y3colorful 25 ease-in-out 5.75s forwards;
}
.y4 {
    color: #fff;
    animation: y4colorful 25 ease-in-out 5.75s forwards;
}

@keyframes y1colorful {
    0% {
        color: #fff;
    }
    100% {
        color: pink;
    }
}
@keyframes y2colorful {
    0% {
        color: #fff;
    }
    100% {
        color: #4cdde2;
    }
}

@keyframes y3colorful {
    0% {
        color: #fff;
    }
    100% {
        color: #ff94a6;
    }
}
@keyframes y4colorful {
    0% {
        color: #fff;
    }
    100% {
        color: yellow;
    }
}

.old {
    color: #fff;
    position: absolute;
    top: 0%;
    animation: old_animation 1s ease-in-out 1s forwards;
    animation-delay: 5.5s;
    margin-left: 20px;
}
@keyframes old_animation {
    0% {
        top: 0%;
    }
    100% {
        top: -500%;
    }
}
.year {
    position: absolute;
    top: 300px;
    width: 100%;
    text-align: center;
    line-height: 1;
    max-width: 600px;
    left: 50%;
    transform: translateX(-50%);
    margin-top: 50px;
}
.year > span {
    font-size: 175px;
    font-weight: 700;
    font-family: "Poppins", sans-serif;
    letter-spacing: 2px;
}
.first_year {
    margin-right: 20px;
}
.new {
    position: absolute;
    right: -210px;
    opacity: 0;
    animation: new_animation 5.1s ease-in-out 1.5s forwards;
}

@keyframes new_animation {
    0% {
        right: -200px;
    }
    50% {
        right: -100px;
        opacity: 1;
    }
    70% {
        right: -120px;
        opacity: 1;
    }
    100% {
        opacity: 1;
        right: 20px;
        color: yellow;
    }
}

.balloon {
    width: 100px;
    height: 120px;
    border-radius: 50%;
    background-color: blue;
    position: absolute;
    top: 50%;
    right: -230px;
    margin-top: -285px;
    animation: balloon 5s ease-in-out 1.5s forwards;
    opacity: 0;
}

.balloon:after {
    content: "";
    width: 4px;
    height: 100px;
    background-color: #fff;
    position: absolute;
    left: 50%;
    margin-left: -2px;
    bottom: -100px;
}
.balloon:before {
    content: "";
    border-style: solid;
    border-width: 0 10px 20px 10px;
    border-color: transparent transparent O#fd3553 transparent;
    position: absolute;
    left: 50%;
    bottom: -10px;
    margin-left: -10px;
}

@keyframes balloon {
    0% {
        right: -230px;
        opacity: 0;
    }
    50% {
        right: -120px;
        opacity: 1;
    }
    80% {
        opacity: 1;
        right: 10px;
        top: 50%;
    }
    100% {
        opacity: 0;
        right: 10px;
        top: -500%;
    }
}

.firework {
    position: relative;
    opacity: 0;
    animation: show_fireworks 2s ease-in-out 5s forwards;
}

@keyframes show_fireworks {
    0% {
        opacity: 0;
    }
    99% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}
.cracker {
    position: absolute;
    width: 4px;
    height: 80px;
    transform-origin: 50% 100%;
    overflow: hidden;
}

.cracker:before {
    content: "";
    background-color: rgb(255, 255, 0);
    height: 40px;
    position: absolute;
    left: 0;
    right: 0;
    animation: fire 2s ease-in-out infinite;
}
@keyframes fire {
    0% {
        top: 100%;
    }
    25% {
        top: 50%;
    }
    50% {
        top: -25%;
    }
    70% {
        top: -50%;
    }
    100% {
        top: -50%;
    }
}

.cracker:nth-child(1) {
    transform: rotate(0deg) translateY(-15px);
}
.cracker:nth-child(2) {
    transform: rotate(30deg) translateY(-15px);
}
.cracker:nth-child(3) {
    transform: rotate(60deg) translateY(-15px);
}
.cracker:nth-child(4) {
    transform: rotate(90deg) translateY(-15px);
}
.cracker:nth-child(5) {
    transform: rotate(120deg) translateY(-15px);
}
.cracker:nth-child(6) {
    transform: rotate(150deg) translateY(-15px);
}
.cracker:nth-child(7) {
    transform: rotate(180deg) translateY(-15px);
}
.cracker:nth-child(8) {
    transform: rotate(210deg) translateY(-15px);
}
.cracker:nth-child(9) {
    transform: rotate(240deg) translateY(-15px);
}
.cracker:nth-child(10) {
    transform: rotate(270deg) translateY(-15px);
}
.cracker:nth-child(11) {
    transform: rotate(300deg) translateY(-15px);
}
.cracker:nth-child(12) {
    transform: rotate(330deg) translateY(-15px);
}

#firework1 {
    left: 25%;
    top: 50%;
    transform: scale(1);
}
#firework2 {
    left: 50%;
    top: 75%;
    transform: scale(0.5);
}
#firework3 {
    left: 27%;
    top: 15%;
    transform: scale(0.3);
}
</style>
