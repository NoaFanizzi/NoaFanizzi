<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <link
      href="https://fonts.googleapis.com/css2?family=Source+Code+Pro&amp;display=swap"
      rel="stylesheet"
    />
    <title>Startpage</title>
  </head>

  <body>
    <div class="wrapper">
      <div class="bg"></div>
      <div class="maincard">
        <div class="content">
          <div class="image">
            <img id="img" src="images/gif.gif" alt="No image" />
          </div>
          <div id="links" class="links">
            <section>
              <h3>Daily</h3>
              <ul>
                <li><a href="https://www.youtube.com/">Youtube</a></li>
                <li><a href="https://github.com">Github</a></li>
                <li><a href="https://web.whatsapp.com/">Whatsapp</a></li>
                <li><a href="https://web.telegram.org/z/">Telegram</a></li>
              </ul>
            </section>
            <section>
              <h3>Social</h3>
              <ul>
                <li><a href="https://twitter.com/">Twitter</a></li>
                <li><a href="https://www.reddit.com/">Reddit</a></li>
                <li><a href="https://Instagram.com">Instagram</a></li>
                <li><a href="https://discord.com/app">Discord</a></li>
              </ul>
            </section>
            <section>
              <h3>Coding</h3>
              <ul>
                <li><a href="https://www.w3schools.com/">W3School</a></li>
                <li><a href="https://leetcode.com">LeetCode</a></li>
                <li><a href="https://hackerrank.com">HackerRank</a></li>
                <li><a href="https://FreeCodeCamp.org">FreeCodeCamp</a></li>
              </ul>
            </section>
            <section>
              <h3>Google</h3>
              <ul>
                <li><a href="https://mail.google.com/mail/u/0/">Gmail</a></li>
                <li><a href="https://drive.google.com">Drive</a></li>
                <li><a href="https://maps.google.com">Maps</a></li>
                <li><a href="https://github.com/Nainish-Rai">Custom</a></li>
              </ul>
            </section>
          </div>
        </div>
        <div class="search">
          <form action="https://search.brave.com/search/">
            <label for="q" autofocus>> find / </label>
            <input
              type="text"
              placeholder="Type Here"
              name="q"
              autocomplete="off"
              autofocus
            />
          </form>
        </div>
      </div>
    </div>
  </body>
  <script>

    function changeCSS(cssFile, cssLinkIndex) {
      console.log("Onclick working");
     var oldlink = document.getElementsByTagName("link").item(cssLinkIndex);
     var newlink = document.createElement("link");
        newlink.setAttribute("rel", "stylesheet");
        newlink.setAttribute("type", "text/css");
        newlink.setAttribute("href", `../${cssFile}/style.css`);
        changeImgSrc(cssFile);
        document.getElementsByTagName("head").item(cssLinkIndex).replaceChild(newlink, oldlink);
}
    function changeImgSrc(cssFile){
        var img_bar=document.getElementById("img");
        img_bar.src=`../${cssFile}/images/gif.gif`;
    }
</script>
</html>

@import url(https://fonts.googleapis.com/css2?family=Source+Code+Pro);
:root {
  --background-color: aqua;
  --link-hover: rgb(19, 217, 252);
  --link-heading: aqua;
  --background-glow: 0px 0px 30px aqua;
}
* {
  padding: 0;
  margin: 0;
}
html {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
body {
  background-color: rgb(36, 36, 36);
  font-family: "Source Code Pro", monospace;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  position: relative;
  overflow-x: hidden;
}
.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 4rem;
  margin-top: -1rem;
}
.maincard {
  display: flex;
  flex-direction: column;
  background-color: rgba(35, 35, 35, 0.902);
  margin-top: 10%;
  height: 800px;
  width: 700px;
  backdrop-filter: blur(7px);
  box-shadow: 0px 0px 40px rgb(0, 0, 0);
}
.content {
  display: flex;
  gap: 3rem;
}
.image {
  max-width: 50%;
  margin-right: 60px;
}
img {
  max-height: 680px;
  max-width: 400px;
  height: 680px;
  padding-left: 10px;
  width: 400px;
  padding-top: 15px;
}
section {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.links {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  gap: 1.5rem;
  width: 300px;
  margin-top: 1rem;
  padding-top: 5px;
  margin-left: 40px;
  color: aliceblue;
  font-size: 20px;
  font-weight: 100;
  border-color: rgba(255, 255, 255, 0);
  border-style: solid;
  border-width: 2px;
}
.links ul {
  display: flex;
  flex-direction: column;
  gap: 0.12rem;
}
.links h3 {
  color: var(--link-heading);
  font-weight: 600;
  align-items: center;
  display: flex;
}
a:hover {
  color: var(--link-hover);
  transform: scale(2);
  margin-bottom: 2px;
  font-weight: 500;
}

a {
  padding: 0px;
  text-decoration: none;
  color: aliceblue;
}
form {
  font-size: 2.5rem;
  margin-bottom: 0px;
  padding-top: 0px;
  border: none;
  color: var(--link-heading);
}

form input {
  border: none;
  background-color: rgba(107, 102, 255, 0);
  color: #aaa;
  font-size: 30px;
  font-weight: 500;
}
form input:focus {
  outline: none;
}
.search {
  display: flex;
  align-items: center;
  margin-top: 1.5rem;
  margin-left: 1rem;
}
.bg {
  height: 780px;
  position: fixed;
  width: 700px;
  margin-left: -5rem;
  margin-top: -2rem;
  background-color: var(--background-color);
  box-shadow: var(--background-glow);
}

/* Hamburger Menu */
.navbar {
  position: fixed;
  top: 0;
  right: 0;
  opacity: 0.95;
}

.navbar-container input[type="checkbox"],
.navbar-container .hamburger-lines {
  display: block;
  cursor: pointer;
}

.navbar-container {
  display: block;
  position: relative;
  height: 64px;
}

.navbar-container input[type="checkbox"] {
  position: absolute;
  display: block;
  height: 32px;
  width: 30px;
  top: 20px;
  left: 20px;
  z-index: 5;
  opacity: 0;
}

.navbar-container .hamburger-lines {
  cursor: pointer;
  display: block;
  height: 15px;
  width: 20px;
  position: absolute;
  top: 17px;
  left: 20px;
  z-index: 2;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.hamburger-lines {
  width: 0.5rem;
  height: 1rem;
}

.navbar-container .hamburger-lines .line {
  cursor: pointer;
  display: block;
  height: 2px;
  width: 100%;
  border-radius: 10px;
  background: rgba(113, 113, 113, 0.503);
}

.navbar-container .hamburger-lines .line1 {
  transform-origin: 0% 0%;
  transition: transform 0.4s ease-in-out;
}

.navbar-container .hamburger-lines .line2 {
  transition: transform 0.2s ease-in-out;
}

.navbar-container .hamburger-lines .line3 {
  transform-origin: 0% 100%;
  transition: transform 0.4s ease-in-out;
}

.navbar .menu-items {
  padding-top: 100px;
  background: rgb(36, 36, 36);
  height: 100vh;
  max-width: 300px;
  transform: translate(150%);
  display: flex;
  flex-direction: column;
  margin-left: -40px;
  padding-left: 50px;
  transition: transform 0.5s ease-in-out;
  box-shadow: 5px 0px 10px 0px var(--background-color);
  list-style: none;
}

.navbar .menu-items li {
  margin-bottom: 1.5rem;
  font-size: 1rem;
  font-weight: 500;
  padding-right: 2rem;
}

.navbar .menu-items li a {
  color: var(--background-color);
}

.navbar .menu-items li a:hover {
  cursor: pointer;
  color: var(--link-hover);
}

.navbar-container input[type="checkbox"]:checked ~ .menu-items {
  transform: translateX(0em);
}

.navbar-container input[type="checkbox"]:checked ~ .hamburger-lines .line1 {
  transform: rotate(35deg);
}

.navbar-container input[type="checkbox"]:checked ~ .hamburger-lines .line2 {
  transform: scaleY(0);
}

.navbar-container input[type="checkbox"]:checked ~ .hamburger-lines .line3 {
  transform: rotate(-35deg);
}
