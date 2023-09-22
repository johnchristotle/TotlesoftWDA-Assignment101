## Totlesoft Web Development Academy (TWDA) Assignment 101
** Design A Simple Responsive Website with HTML and CSS Only ** 

[by Agholor Christotle](https://github.com/johnchristotle)


This is a simple project to text your ability after the HTML and CSS basic classes.

### Marketplace

![Landing Page Screenshot](./images/assign101.jpg)


As a beginner in web development, seeking to acquiring knowledge in web development, one of the crucial skills for learners is the ability to build both simple and complex websites. A strong skill for learners is the capability to create a website using only HTML and CSS, without relying on frameworks like Bootstrap.

A website is simply a collection of digital resources, such as web pages and related stuff. It is a digital platform with interactive features, multimedia, and text that is designed to provide users with a variety of information, services, or resources.

In this Assignment, you are to design a contemporary and visually appealing website using HTML and CSS only. The website should feature a logo, a navigation bar, a sidebar menu, and a curved design at the bottom. Additionally, it will be responsive, ensuring it adapts well to different devices and screen sizes as well as have a simple animation effect.

A video tutorial and demo of the website has been uploaded to our Youtube Page [Video Tutorial](https://youtube.com/@iamchristotle) in order to guide you through the process of creating a straightforward, responsive website using HTML and CSS with all the basic features you have been taught so far. Each step will be clearly demonstrated, allowing you to follow along where you are having any challenge.


## Steps To Creating A Simple Responsive Website with HTML and CSS Only

### Source Code:

* A. [Source Code: GitHub](https://github.com/johnchristotle/TotlesoftWDA-Assignment101.git)

* B. [Source Code: Google Drive](https://drive.google.com/drive/folders/1gDhq3O89ogVDpDmqpymYfwJT6ivE7Y6i?usp=sharing)


### Let's Begin:

* 1. Create a folder. (You can name this folder whatever you want, and inside this folder, create the mentioned files).

* 2. Create an index.html file. The file name must be index and its extension .html

* 3. Create a styles.css file. The file name must be styles and its extension .css

* 4. A. **Source Code from Google Drive? ** 
* Download the images folder from google drive and put this folder inside the project folder. This folder has all the images that will be used for this website.

* 4. B. ** Source Code from GitHub? **
* Clone the project locally, change into the directory, and install the dependencies:

```sh
git clone https://github.com/johnchristotle/TotlesoftWDA-Assignment101.git

cd TotlesoftWDA-Assignment101

```

## If you are using just the image resource and doing the coding yourself without using the code from the source (Recommended):

* Begin by adding the following HTML codes to your index.html file: The provided code segment consists of a website header and an unordered list (ul) for website navigation. It also includes a hamburger button that allows toggling of the website’s sidebar in the mobile version and images.

```HTML-CODE
<!DOCTYPE html>
<!-- Coding by Christotle Agholor || https://totlesoft.com -->
<html lang="en">
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Project 101: Responsive Website with HTML & CSS Only</title>
    <link rel="stylesheet" href="styles.css" />
    <script src="../custom-scripts.js" defer></script>
  </head>
  <body>
    <main>
      <!-- Header Start -->
      <header>
        <nav class="nav container">
          <h2 class="nav_logo"><a href="#">Totle<span class="soft">Soft</span></a></h2>

          <ul class="menu_items">
            <img src="images/times.svg" alt="timesicon" id="menu_toggle" />
            <li><a href="#" class="nav_link">Home</a></li>
            <li><a href="#" class="nav_link">About</a></li>
            <li><a href="#" class="nav_link">Products</a></li>
            <li><a href="#" class="nav_link">Blog</a></li>
            <li><a href="#" class="nav_link">Contact</a></li>
          </ul>
          <img src="images/bars.svg" alt="timesicon" id="menu_toggle" />
        </nav>
      </header>
      <!-- Header End -->

      <!-- Hero Start -->
      <section class="hero">
        <div class="row container">
          <div class="column">
            <h2>WEB DEVELOPMENT <br /><span class="soft">Training</span></h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Perferendis, architecto? Consectetur enim obcaecati velit quibusdam iure, perspiciatis accusantium, voluptatibus possimus cum voluptates dolorum optio ab vitae. Praesentium voluptas quia voluptates at aperiam aliquid vitae autem!</p>
            <div class="buttons">
              <button class="btn">Read More</button>
              <button class="btn">Contact Us</button>
            </div>
          </div>
          <div class="column">
            <img src="images/hero.png" alt="heroImg" class="hero_img" />
          </div>
        </div>
        <img src="images/bg-bottom-hero.png" alt="" class="curveImg" />
      </section>
      <!-- Hero End-->
    </main>

    <script>
      const header = document.querySelector("header");
      const menuToggler = document.querySelectorAll("#menu_toggle");

      menuToggler.forEach(toggler => {
        toggler.addEventListener("click", () => header.classList.toggle("showMenu"));
      });
    </script>
  </body>
</html>
```

* Next: add the following CSS codes to your style.css file to apply visual styling to your website. You can customize this code to your liking by adjusting the color, font, size, and other CSS properties as you have been taught:

```CSS-CODE
/* Import Google font - Poppins */
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600;700&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}
main {
  background: linear-gradient(#1a043f, #1e0644, maroon);
  background-repeat: no-repeat;
  background-attachment: fixed;
}

.container {
  max-width: 1300px;
  width: 100%;
  margin: 0 auto;
}

header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
}
.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 60px;
}
.nav_logo {
  padding: 10px 0;
}
.soft{
  color: rgb(228, 207, 23);
}
.menu_items {
  display: flex;
  list-style: none;
  gap: 20px;
}
a {
  color: #fff;
  text-decoration: none;
}

a:hover{
  color: rgb(228, 207, 23);
 
}

a:focus{
  color: rgb(228, 207, 23);
 
}

/* Hero */
.hero {
  position: relative;
  min-height: 100vh;
  width: 100%;
  background: url(images/bg-dot.png), url(images/bg-dot.png), url(images/bg-round.png), url(images/bg-tree.png);
  background-position: 20px 20px, bottom 215px right 10px, left 55% top -1%, left 45% bottom -1px;
  background-repeat: no-repeat;
}
.curveImg {
  position: absolute;
  bottom: 0;
  width: 100%;
  pointer-events: none;
}
.hero .row {
  display: flex;
  align-items: center;
  min-height: 100vh;
  height: 100%;
  width: 100%;
  padding: 0 60px;
  gap: 30px;
  justify-content: space-between;
}

h2{
  line-height:55px;

}

p{
  font-weight: 200;
}
.hero .row h2,
.hero .row p {
  color: #fff;
}
.hero .row h2 {
  font-size: 46px;
  margin-bottom: 16px;
}
.hero .column {
  width: 50%;
}
.buttons {
  display: flex;
  margin-top: 25px;
  gap: 10px;
}
.btn {
  padding: 14px 26px;
  background: #fff;
  border-radius: 50px;
  border: none;
  cursor: pointer;
  transition: all 0.3s ease;
  font-weight: 600;
}
.btn:last-child {
  border: 2px solid rgb(228, 207, 23);
  background: transparent;
  color: rgb(228, 207, 23);
}
.btn:last-child:hover {
  background-color: rgb(228, 207, 23);
  color: #000;
  font-weight: 600;
}
.hero_img {
  width: 100%;
  z-index: 10;
  position: relative;

  animation: christotleX;
  animation-duration: 3s;
  animation-timing-function: ease-out;
}

@keyframes christotleX{
  from{margin-left: 100%;}
  to{margin-right: 0%;}
}

#menu_toggle {
  display: none;
}

/* Reponsive */
@media (width < 860px) {
  #menu_toggle {
    display: block;
  }
  .nav {
    padding: 0 20px;
    background-color: #fff;
  }

  .menu_items {
    position: fixed;
    top: 0;
    width: 260px;
    background-color: #fff;
    height: 100%;
    left: -100%;
    padding: 50px 30px 30px;
    flex-direction: column;
    transition: all 0.5s ease;
  }
  .showMenu .menu_items {
    left: 0;
  }
  a {
    color: #1a1919;
  }

  a:focus{
    color: rgb(29, 18, 179);
   
  }
  
  #menu_toggle {
    width: 20px;
    cursor: pointer;
  }
  .menu_items #menu_toggle {
    position: absolute;
    top: 20px;
    right: 20px;
  }
  .hero {
    padding-top: 130px;
  }
  .hero .row {
    flex-direction: column;
    padding: 0 20px;
    justify-content: center;
  }
  .hero .row .column {
    width: 100%;
  }
}

@media (width < 600px) {
  .hero {
    padding-top: 80px;
  }
  .hero .row h2 {
    font-size: 26px;
  }
  .buttons {
    justify-content: center;
  }
  .btn {
    padding: 10px 16px;
  }
}
```


### Conclusion

In conclusion, creating a responsive website with a modern feel allows you to apply your skills to a real-world website. We believe that by following the steps in this guide, you’ve successfully created your own website using HTML and CSS; thus Completed your first Project successfully. Congratulations.

### Note:
If by any chance you encounter any difficulties while creating your own Website or if your code did not working as expected, you can download the source code files for this website for free by using the links provided above.


## Totlesoft
* [totlesoft.com](https://totlesoft.com)
...where the magic happens!
