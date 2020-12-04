<template>
  <router-view />
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Roboto:300,400,500,700&display=swap");

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-weight: 400;
}
.contain {
  position: relative;
}
.overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  pad: 10px;
  transition: 0.5s ease;
  background-color: black;
  border-radius: 0.6rem;
}

.contain .overlay {
  opacity: 0.5;
}

.text {
  // z-index: 1252;
  position: absolute;
  text-align: left !important;
  bottom: 0 !important;
  margin-left: 18px;
}

.main {
  display: block;
  max-width: 900px;
  columns: 15rem;
  gap: 1.3rem;
}

.main .figure {
  margin-bottom: 1rem;
  break-inside: avoid;
}

* {
  box-sizing: border-box;
}

body {
  font-family: avenir, roboto, helvetica, sans-serif;
  margin: 2rem calc(2vw + 2rem);
}

img {
  min-height: 280px;
  width: 100%;
  display: block;
  border-radius: 0.6rem;
}

figure {
  margin: 0;
}

figcaption {
  padding: 0.5rem 1rem 0.4rem;
  background: #ddd;
  color: #333;
  border-radius: 0.6rem;
  text-align: end;
}

#myImg {
  border-radius: 5px;
  cursor: pointer;
  transition: 0.3s;
}

#myImg:hover {
  opacity: 0.7;
}

/* The Modal (background) */
.modal {
  display: block; /* Hidden by default */
  position: fixed; /* Stay in place */
  z-index: 1031;
  padding-top: 100px; /* Location of the box */
  left: 0;
  top: 0;
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  background-color: rgb(53, 52, 52); /* Fallback color */
  background-color: rgba(59, 58, 58, 0.9); /* Black w/ opacity */
}

/* Modal Content (image) */
.modal-content {
  margin: auto;
  display: block;
  width: 100%;
  border-radius: 8px;
  max-width: 900px;
  height: 80%;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: center;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  overflow: hidden;
  object-fit: cover;
}

/* Caption of Modal Image */
#caption {
  margin: auto;
  display: block;
  width: 100%;
  max-width: 900px;
  text-align: center;
  color: #ccc;
  padding-top: 15px;
  padding-bottom: 15px;
  padding-left: 30px;
  padding-right: 30px;
  border-bottom-left-radius: 8px;
  border-bottom-right-radius: 8px;
  height: 70px;
}

/* Add Animation */
.modal-content,
#caption {
  -webkit-animation-name: zoom;
  -webkit-animation-duration: 0.6s;
  animation-name: zoom;
  animation-duration: 0.6s;
}

@-webkit-keyframes zoom {
  from {
    -webkit-transform: scale(0);
  }
  to {
    -webkit-transform: scale(1);
  }
}

@keyframes zoom {
  from {
    transform: scale(0);
  }
  to {
    transform: scale(1);
  }
}

/* The Close Button */
.close {
  position: absolute;
  top: 35px;
  right: 35px;
  color: #f1f1f1;
  font-size: 16px;
  // font-weight: bold;
  transition: 0.3s;
}

.close:hover,
.close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}

/* 100% Image Width on Smaller Screens */
@media only screen and (max-width: 700px) {
  .modal-content {
    width: 100%;
  }
}
.padm {
  position: absolute;
  text-align: left !important;
  bottom: 0 !important;
  padding-bottom: 6px;
  z-index: 1030;
}
.lwm {
  background-color: #e6e6e6;
  color: #e6e6e6;
  line-height: 1;
  margin-bottom: 2px !important;
  width: 50%;
  z-index: 1031;
}
.bwm {
  background-color: #e6e6e6;
  color: #e6e6e6;
  line-height: 1;
  margin-bottom: 1px !important;
  width: 100%;
  z-index: 1031;
}
.lwme {
  font-size: 13px;
  color: #fff;
  font-weight: 500;
}
.bwme {
  font-size: 15px;
  color: #fff;
  font-weight: 700;
  line-height: 1;
  margin-bottom: 0px !important;
}
.padme2 {
  position: absolute;
  text-align: left !important;
  bottom: 0 !important;
  z-index: 1032;
  background-color: #fff;
}
.lwme2 {
  font-size: 13px;
  color: #111;
  font-weight: 500;
}
.bwme2 {
  font-size: 15px;
  color: #111;
  font-weight: 700;
  line-height: 1;
  margin-bottom: 5px !important;
}
.loadAnim {
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: #bbb;
  border-radius: 5px;
  opacity: 0.5;
  -webkit-animation-name: zoom;
  -webkit-animation-duration: 6s;
  animation-name: zoom;
  animation-duration: 6s;
}
#color-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: black;
  border-radius: 5px;
  opacity: 0.8;
}
.under {
  margin-left: 35px;
  margin-right: 28px !important;
}
.myCol2 {
  text-align: left !important;
  flex: 0 0 28%;
  max-width: 30.638%;
  min-width: 28%;
  background-color: #dfdede;
}
.myGrid2 {
  margin-top: 0px !important;
  margin-left: 13px;
  margin-right: 13px;
  margin-bottom: 26px;
  min-height: 300px;
  max-height: 320px;
  background: #f5f5f5;
  //   border: 1px #fff;
  border-radius: 5px;
  border-color: hsla(0, 0%, 0%, 0.7);
  counter-increment: item;
}
.myCol {
  text-align: left !important;
  flex: 0 0 28%;
  max-width: 30.638%;
  min-width: 28%;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: center;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  overflow: hidden;
  object-fit: cover;
  flex-shrink: 0;
  cursor: pointer;
}
.myGrid {
  margin-top: 0px !important;
  margin-left: 13px;
  margin-right: 13px;
  margin-bottom: 26px;
  //   width: 30%;
  min-height: 300px;
  max-height: 320px;
  background: #fff;
  //   border: 1px #fff;
  border-radius: 5px;
  border-color: hsla(0, 0%, 0%, 0.7);
  counter-increment: item;
}
.row2 {
  display: flex;
  flex-wrap: wrap;
  margin-left: 17%;
  margin-right: 17%;
  padding-left: 70px;
  padding-right: 70px;
}
.propp {
  font-size: 26px;
  font-weight: 600;
  color: #253858;
}
.coolor {
  color: #6d7b91;
  margin-left: 7px;
}
.minus {
  margin-top: -35px;
  transition: all 0.1s ease-in-out;
}
.bckLay {
  margin-left: 12%;
  margin-right: 12%;
  background-color: #dde2e9;
  padding-top: 120px;
  padding-bottom: 100px;
  padding-left: 70px;
  padding-right: 70px;
  min-height: 185px !important;
  max-height: 185px !important;
}
._2FayZ {
  border-radius: 8px;
  background-color: #fff;
}
@media (max-width: 814px) {
  .myCol {
    flex: 0 0 40.65%;
    max-width: 50.276%;
    min-width: 40.65%;
  }
}
@media (max-width: 583px) {
  .myCol {
    flex: 0 0 80.65%;
    max-width: 80.276%;
    min-width: 80.65%;
  }
  .under {
    margin-left: 0px !important;
    margin-right: 28px;
  }
}
@media (max-width: 411px) {
  .myCol {
    flex: 0 0 94.65%;
    max-width: 94.276%;
    min-width: 94.65%;
  }
  .row2 {
    margin-left: 8% !important;
    margin-right: 10%;
  }
  .under {
    margin-left: 0px !important;
    margin-right: 0px !important;
  }
  .bckLay {
    padding: 10px;
    max-height: 95px !important;
  }
}
@media (max-width: 1200px) {
  .under {
    margin-left: 15px;
    margin-right: 28px;
  }
}
@media (min-width: 768px) {
  ._2FayZ {
    height: 54px;
  }
  .bckLay {
    background-color: #dde2e9;
    padding: 40px;
    min-height: 185px !important;
    max-height: 185px !important;
  }
  .row2 {
    display: flex;
    flex-wrap: wrap;
    margin-left: 12%;
    margin-right: 12%;
    padding-left: 50px;
    padding-right: 50px;
  }
}
@media (max-width: 768px) {
  .bckLay {
    background-color: #dde2e9;
    padding: 20px;
    max-height: 95px !important;
  }
  .minus {
    margin-top: -35px;
    transition: all 0.1s ease-in-out;
  }
  .row2 {
    display: flex;
    flex-wrap: wrap;
    margin-left: 15%;
    margin-right: 15%;
    padding-left: 50px;
    padding-right: 50px;
  }
}
._3SiJv {
  position: relative;
}
.mV0BM {
  margin-top: 20px;
  margin-bottom: 20px;
  margin-left: 20px;
  margin-right: 20px;
  display: flex;
  min-height: 54px;
  transition: all 0.1s ease-in-out;
}

.mV0BM2 {
  margin-top: 8px;
  margin-bottom: 8px;
  margin-left: 23px;
  margin-right: 23px;
  display: flex;
  transition: all 0.1s ease-in-out;
}

._1kw5X:hover,
._1rBwv {
  color: #fff;
}
._2VoZY {
  margin-left: 13px;
  margin-right: 13px;
  display: flex;
  align-items: center;
}
._3d86A,
._3d86A:hover {
  box-shadow: none;
}
._3d86A {
  border: none;
  padding: 0;
  background-color: initial;
  text-align: inherit;
}
button,
input,
optgroup,
select,
textarea {
  line-height: inherit;
}
button {
  color: inherit;
  cursor: pointer;
}
button,
select {
  text-transform: none;
}
button,
input {
  overflow: visible;
}
button,
input,
optgroup,
select,
textarea {
  font-family: inherit;
  font-size: 100%;
  line-height: 1.15;
  margin: 0;
}
._2ZbDJ {
  flex-grow: 1;
  display: flex;
}
._3FYu1:required {
  box-shadow: none;
}
.zbIrd {
  padding-left: 12px;
}
._3FYu1 {
  box-sizing: border-box !important;
}
._3FYu1 {
  flex-grow: 1;
  width: 100%;
  background: none;
  border: none;
  color: #111;
}
[type="search"] {
  -webkit-appearance: textfield;
  outline-offset: -2px;
}
button,
input,
optgroup,
select,
textarea {
  line-height: inherit;
}
input {
  letter-spacing: inherit;
}
button,
input {
  overflow: visible;
}
button,
input,
optgroup,
select,
textarea {
  font-family: inherit;
  font-size: 100%;
  line-height: 1.15;
  margin: 0;
}
</style>
