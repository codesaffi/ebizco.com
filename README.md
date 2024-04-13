<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>EBIZCO</title>

    <link rel="stylesheet" href="index.css" />
    <link
      href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css"
      rel="stylesheet"/>
      <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
      <style>
      *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    text-decoration: none;
    border: none;
    outline: none;
    scroll-behavior: smooth;
    font-family: "Poppins", sans-serif;
}
:root{
    --bg-color:#000000;
    --second-bg-color: #131313;
    --text-color: white;
    --main-color:#00ffee;
}
html{
    font-size: 60%;
    overflow-x: hidden;
}
body{
    background: var(--bg-color);
    color: var(--text-color);
}
.header{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 4rem 12% 4rem;
    background: rgba(0, 0, 0, 0.3);
    backdrop-filter: blur(10px);
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 5;
}
.logo{
    font-size: 3rem;
    color: var(--text-color);
    font-weight: 800;
    cursor: pointer;
    transition: 0.5s ease;
}
.logo:hover{
    transform: scale(1.1);
}
.logo span{
    text-shadow: 0 0 25px var(--main-color);
}
.navbar a{
    font-size: 1.8rem;
    color: var(--text-color);
    margin-left: 4rem;
    font-weight: 500;
    transition: 0.3s ease;
    border-bottom: 3px solid transparent;
              /* display: block; */
}
.navbar a:hover,
.navbar a.active{
    color: var(--main-color);
    border-bottom: 3px solid var(--main-color);
}
#menu-icon{
    /* font-size: 3.6rem;
    color: var(--main-color); */
    display: none;
}
section{
    min-height: 100vh;
    padding: 10rem 12% 10rem;
}
.home{
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 15rem;
}
.home-content{
    display: flex;
    flex-direction: column;
    align-items: baseline;
    text-align: left;
    justify-content: center;
    margin-top: 3rem;
}
span{
    color: var(--main-color)
}
.logo span{
    color: var(--main-color);
}
.home-content  h3{
    margin-bottom: 2rem;
    margin-top: 1rem;
    font-size: 3.5rem;
}
.home-content h1{
    font-size: 7rem;
    font-weight: 700;
    margin-top: 1.5rem;
    line-height: 1;
}
.home-img img{
    position: relative;
    top: 3rem;
    height: 60vh;
    width: 32vw;
    border-radius: 50%;
    box-shadow: 0 0 17px var(--main-color);
    cursor: pointer;
    transition: 0.4s ease-in-out;
}
.home-img img:hover{
    box-shadow: 0 0 25px var(--main-color),
                0 0 50px var(--main-color),
                0 0 100px var(--main-color);
}
.home-content p{
    font-size: 1.5rem;
    font-weight: 500;
    line-height: 1.6;
    max-width: 1000px;
}
.social-icons a{
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 4.5rem;
    height: 4.5rem;
    background: transparent;
    border: 2px solid var(--main-color);
    font-size: 2.5rem;
    border-radius: 50%;
    color: var(--main-color);
    margin: 3rem 1.5rem 3rem 0;
    transition: 0.3s ease-in-out;
}
.social-icons a:hover{
    color: var(--text-color);
    transform: scale(1.3)translateY(-5px);
    box-shadow: 0 0 25px var(--main-color);
    background-color: var(--main-color);
}
.btn{
    display: inline-block;
    padding: 1rem 2.8rem;
    background: var(--main-color);
    box-shadow: 0 0 25px var(--main-color);
    border-radius: 4rem;
    font-size: 1.6rem;
    color: black;
    border: 2px solid transparent;
    letter-spacing: 0.1rem;
    font-weight: 600;
    transition: 0.3 ease-in-out;
    cursor: pointer;
}
.btn:hover{
    transform: scale(1.05);
    box-shadow: 0 0 50px var(--main-color);
}
.btn-group{
    display: flex;
    align-items: center;
    gap: 1.5rem;
}
.btn-group a:nth-of-type(2){
    background: black;
    color: var(--main-color);
    border: 2px solid var(--main-color);
    box-shadow: 0 0 25px transparent;
}
.btn-group a:nth-of-type(2):hover{
    box-shadow: 0 0 25px var(--main-color);
    background-color: var(--main-color);
    color: black;
}
.text-animation{
    font-size: 34px;
    font-weight: 600;
    min-width: 280px;
}
.text-animation span{
    position: relative;
}
.text-animation span::before{
    content: "web developer";
    color: var(--main-color);
    animation: words 20s infinite;
}
.text-animation span::after{
    content: "";
    background-color: var(--bg-color);
    position: absolute;
    width: calc(100% + 8px);
    height: 100%;
    border-left: 3px solid var(--bg-color);
    right: -8px;
    animation: cursor 0.6s infinite,typing  20s steps(14) infinite;
}

@keyframes cursor{
    to{
        border-left: 2px solid var(--main-color);
    }
}

@keyframes words{
    0%,
    20%{
        content: "copywritter";
    }
    21%,
    40%{
        content: "social media marketer";
    }
    41%,
    60%{
        content: "web developer";
    }
    61%,
    80%{
        content: "graphic designer";
    }
    81%,
    100%{
        content: "social media manager";
    }
}

@keyframes typing{
    10%,
    15%,
    30%,
    35%,
    50%,
    55%,
    70%,
    75%,
    90%,
    95%{
        width: 0;
    }
    5%,
    20%,
    25%,
    40%,
    45%,
    60%,
    65%,
    80%,
    85%{
        width: calc(100% + 8px);
    }
} 
.heading{
    font-size: 7rem;
    text-align: center;
    margin: 5rem 0;
}
.education{
    padding: 100px 15px;
    background: var(--second-bg-color);
}
.education h2{
    margin-bottom: 5rem;
}
.timeline-items{
    max-width: 1200px;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    position: relative;
}
.timeline-items::before{
    content: "";
    position: absolute;
    width: 5px;
    height: 100%;
    background-color: var(--main-color);
    left: calc(50% - 1px);
}
.timeline-item{
    margin-bottom: 40px;
    width: 100%;
    position: relative;
}
.timeline-item:last-child{
    margin-bottom: 0;
}
.timeline-item:nth-child(odd){
    padding-right: calc(50% + 30px);
    text-align: right;
}
.timeline-item:nth-child(even){
    padding-left: calc(50% + 30px);
}
.timeline-dot{
    height: 21px;
    width: 21px;
    background-color: var(--main-color);
    box-shadow: 0 0 25px var(--main-color),
                0 0 50px var(--main-color);
    position: absolute;
    left: calc(50% - 8px);
    border-radius: 50%;
    top: 10px;
}
.timeline-date{
    font-size: 20px;
    font-weight: 800;
    color: white;
    margin: 6px 0 15px;
}
.timeline-content{
    background-color: var(--bg-color);
    border: 3px solid var(--main-color);
    padding: 30px 50px;
    border-radius: 4rem;
    box-shadow: 0 0 10px var(--main-color);
    cursor: pointer;
    transition: 0.3s ease-in;
}
.timeline-content:hover{
    transform: scale(1.05);
    box-shadow: 0 0 25px var(--main-color);
}
.timeline-content h3{
    font-size: 20px;
    color: white;
    margin: 0 0 10px;
    font-weight: 600;
}
.timeline-content p {
    color: white;
    font-size: 16px;
    font-weight: 300;
    line-height: 22px;
}

::-webkit-scrollbar{
    width: 15px;
}
::-webkit-scrollbar-thumb{
    background-color: var(--main-color);
}
::-webkit-scrollbar-track{
    background-color: var(--bg-color);
    width: 50px;
}
.services{
    background: var(--bg-color);
    color: black;
}
.services h2{
    margin-bottom: 5rem;
    color: white;
}
.services-container{
    display: grid;
    grid-template-columns: repeat(2,1fr);
    align-items: center;
    gap: 2.5rem;
}
.service-box{
    background-color: var(--main-color);
    height: 300px;
    border-radius: 3rem;
    border: 5px solid transparent;
    cursor: pointer;
    transition: 0.4s ease-in-out;
}
.service-box:hover{
    background: white;
    color: black;
    border: 5px solid var(--main-color);
    transform: scale(1.03);
}
.service-box .service-info{
    display: flex;
    flex-direction: column;
    text-align: left;
    max-width: 100%;
    justify-content: left;
    align-items: baseline;
    padding: 2rem 1.9rem;
}
.service-info h4{
    font-size: 3rem;
    font-weight: 800;
    line-height: 1.2;
    padding-bottom: 1.5rem;
}
.service-info p{
    font-size: 1.6rem;
    font-weight: 600;
    max-height: 100px;
    line-height: 1.7;
    margin: auto;
}
.testimonials{
    background: var(--second-bg-color);
}
.testimonials-box{
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}
.testimonials .heading{
    margin-bottom: 5rem;
}
.testimonials-box img{
    width: 15rem;
    border-radius: 50%;
    border: 3px solid var(--main-color);
    box-shadow: 0 0 25px var(--main-color);
}
.wrapper{
    display: grid;
    grid-template-columns: repeat(3,1fr);
    gap: 3rem;
}
.testimonial-item{
    min-height: 550px;
    max-width: 450px;
    background: rgba(0, 0, 0, 0.7);
    border: 3px solid rgba(238, 238, 238, 0.2);
    border-radius: 2rem;
    margin: 0 2rem;
    padding: 30px 60px;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    gap: 1.5rem;
    color: white;
    transition: 0.4s ease-in-out;
}
.testimonial-item:hover{
    border: 3px sloid var(--main-color);
    transform: translateY(-10px)scale(1.03);
    box-shadow: 0 0 50px var(--main-color);
}
.testimonial-item h2{
    font-size: 2.8rem;
}
.testimonial-item p{
    font-size: 1.3rem;
}
#star{
    color: gold;
    font-size: 2rem;
}
.contact{
    background-color: var(--bg-color);
}
.contact h2{
    margin-bottom: 3rem;
    color: white;
    font-size: 7rem;
}
.contact form{
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 3rem;
    margin: 5rem auto;
    text-align: center;
}
.contact form .input-box{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}
.contact form .input-box input,
.contact form textarea{
    width: 100%;
    padding: 2.5rem;
    font-size: 1.8rem;
    color: var(--text-color);
    background: var(--second-bg-color);
    border-radius: 2rem;
    border: 2px solid var(--main-color);
    margin: 1.5rem 0;
    resize: none;
}
.contact form .btn{
    margin-top: 2rem;
}
.footer{
    position: relative;
    bottom: 0;
    width: 100%;
    padding: 40px 0;
    background-color: var(--second-bg-color);
}
.footer .social{
    text-align: center;
    padding-bottom: 25px;
    color: var(--main-color);
}
.footer .social a{
    font-size: 25px;
    color: var(--main-color);
    border: 2px solid var(--main-color);
    width: 42px;
    height: 42px;
    line-height: 42px;
    display: inline-block;
    text-align: center;
    border-radius: 50%;
    margin: 0 10px;
    transition: 0.3s ease-in-out;
}
.footer .social a:hover{
    transform: scale(1.2)translateY(-10px);
    background-color: var(--main-color);
    color: black;
    box-shadow: 0 0 255px var(--main-color);
}
.footer ul{
    margin-top: 0;
    padding: 0;
    font-size: 18px;
    line-height: 1.6;
    margin-bottom: 0;
    text-align: center;
}
.footer ul li a{
    color: white;
    border-bottom: 3px solid transparent;
    transition: 0.3s ease-in-out;
}
.footer ul li a:hover{
    border-bottom: 3px solid var(--main-color);
}
.footer ul li{
    display: inline-block;
    padding: 0 15px;  
}
.footer .copyright{
    margin-top: 50px;
    text-align: center;
    font-size: 16px;
    color: white;
}

@media (max-width:1285px) {
    html{
        font-size: 55%;
    }
    .services-container{
        padding-bottom: 7rem;
        grid-template-columns: repeat(2,1fr);
        margin: 0 5rem;
    }
    .home-img img {
        position: relative;
        top: 3rem;
        height: 50vh;
        width: 25vw;
        border-radius: 50%;
        box-shadow: 0 0 17px var(--main-color);
        cursor: pointer;
        transition: 0.4s ease-in-out;
    }
}
@media(max-width:991px) {
    header{
        padding: 2rem 3%;
    }
    .home-img img {
        position: relative;
        top: 3rem;
        height: 50vh;
        width: 35vw;
        border-radius: 50%;
        box-shadow: 0 0 17px var(--main-color);
        cursor: pointer;
        transition: 0.4s ease-in-out;
    }
    section{
        padding: 10rem 3% 2rem;
    }
    .timeline-items::before{
        left: 7px;
    }
    .timeline-item:nth-child(odd){
        padding-right: 0;
        text-align: left;
    }
    .timeline-item:nth-child(odd),
    .timeline-item:nth-child(even){
        padding-left: 37px;
    }
    .timeline-dot{
        left: 0;
    }
    .services{
        padding-bottom: 7rem;
    }
    .testimonials .wrapper{
        grid-template-columns: repeat(1,1fr);
    }
    .contact form{
        flex-direction: column;
    }
    .footer{
        padding: 2rem 3%;
    }
}
@media (max-width:895px) {
    #menu-icon{
        display: block;
        cursor:pointer;
        font-size: 3.6rem;
        color: var(--main-color);
    }
    .navbar{
        position: absolute;
        top: 100%;
        right: 0;
        width: 50%;
        padding: 1rem 3%;
        background: rgba(0, 0, 0, 0.8);
        backdrop-filter: blur(20px);
        border-bottom-left-radius: 2rem;
        border-left: 2px solid var(--main-color);
        border-bottom: 2px solid var(--main-color);
        display: none;  
        overflow: hidden;
        opacity: 1;  
    }
    .navbar.active{
        display: block;
        opacity: 1;
    }
    .navbar a{
        display: block;
        font-size: 2rem;
        margin: 3rem 0;
        color: white;
    }
    .home{
        flex-direction: column-reverse;
        margin: 5rem 4rem;
    }
    .home-content h3{
        font-size: 2.6rem;
    }
    .home-content h1{
        font-size: 8rem;
        margin-top: 3rem;
    }
    .home-content p{
        max-width: 600;
        margin: 0 auto;
    }
    .home-img img{
        width: 35vw;
        height: 45vh;
    }
    .services h2{
        margin-bottom: 3rem;
    }
    .services-container{
        grid-template-columns: repeat(1,1fr);
    }
    .service-info p {
        font-size: 1.2rem;
        font-weight: 700;
    }
}
@media (max-width:655px){
    .home-img img {
        width: 84vw;
        height: 55vh;
    }
}
      </style>
  </head>
  <body>

    <header class="header">
      <a href="#home" class="logo"><span>ebizco</span></a>

      <i class="bx bx-menu" id="menu-icon"></i>

      <nav class="navbar">
        <a href="#home" class="active">home</a>
        <a href="#education">education</a>
        <a href="#services">services</a>
        <a href="#testimonials">testimonials</a>
        <a href="#contact">contact</a>
      </nav>
    </header>

    <section class="home" id="home">
      <div class="home-content">
        <h1>hi, it's <span>ebizco</span></h1>
        <h3 class="text-animation">i'm a <span></span></h3>
        <p>  Welcome to our online marketing agency, where innovation meets impact! We specialize in crafting digital strategies that propel businesses forward in the ever-evolving online landscape. From social media management to search engine optimization and beyond, we're dedicated to delivering tailored solutions that resonate with your target audience and drive tangible results. With a blend of creativity and data-driven insights, we're here to elevate your brand and amplify your online presence.
        </p>

        <div class="social-icons">
          <a href="#"><i class="bx bxl-linkedin"></i></a>
          <a href="#"><i class='bx bxl-facebook-circle'></i></a>
          <a href="#"><i class="bx bxl-instagram-alt"></i></a>
          <a href="#"><i class="bx bxl-twitter"></i></a>
        </div>

        <div class="btn-group">
          <a href="#" class="btn">hire</a>
          <a href="#contact" class="btn">contact</a>
        </div>
      </div>

      <div class="home-img">
        <img src="Work from Home - 2250x1500.png" alt="" />
      </div>
    </section>

    <section class="education" id="education">
      <h2 class="heading">education</h2>
      <div class="timeline-items">

        <div class="timeline-item">
          <div class="timeline-dot"></div>
            <div class="timeline-date">2021</div>
            <div class="timeline-content">
              <h3>school</h3>
              <p>
                did my matriculation degree from linc school system in batch 2019-2021 passed with A grade
              </p>
            </div>
          
        </div>

        <div class="timeline-item">
          <div class="timeline-dot"></div>
            <div class="timeline-date">2022</div>
            <div class="timeline-content">
              <h3>college</h3>
              <p>
                i have done my intermediate from F.G college in batch 2021-2023 passed with A grade
              </p>
            </div>
          
        </div>

        <div class="timeline-item">
          <div class="timeline-dot"></div>
            <div class="timeline-date">2023</div>
            <div class="timeline-content">
              <h3>online marketing</h3>
              <p>
                marketing has always inspire me i always wanted to help businesses grow online so i started learning digital marketing i learned everything online from youtube,udemy and google courses
              </p>
            </div>
          
        </div>

        <div class="timeline-item">
          <div class="timeline-dot"></div>
            <div class="timeline-date">2024</div>
            <div class="timeline-content">
              <h3>marketing agency</h3>
              <p>
                after learning enough online about marketing and learning skills for marketing started my marketing agency in the start 2024
              </p>
            </div>
          
      </div>
      </div>
    </section>

     <section class="services" id="services">
      <h2 class="heading">services</h2>

       <div class="services-container">
        <div class="service-box">
          <div class="service-info">
            <h4>copy writting</h4>
            <p>Crafting compelling narratives is our forte, a wordsmith who weaves magic into every sentence. With a penchant for persuasion and an eye for detail, We breathe life into brands and captivate audiences. We are the architect of stories, sculpting messages that resonate and inspire action. Let us be the voice that elevates your brand to new heights.</p>
          </div>
        </div>

        <div class="service-box">
          <div class="service-info">
            <h4>website development</h4>
            <p>From concept to launch, we turn ideas into sleek, functional websites that make an impact. Let's create something amazing together.We provide you with a modren design website that will help you stay connected with your clients. In the time of technology an elegent website will make you stay ahead of your competitors</p>
          </div>
        </div>

        <div class="service-box">
          <div class="service-info">
            <h4>social media managemnet</h4>
            <p>We specialize in social media management, turning platforms into powerful tools for engagement and growth. With a keen understanding of trends and analytics, we craft strategies that amplify brands and foster meaningful connections. From content creation to community building, we're here to elevate your online presence and drive results. Let's make your brand shine in the digital spotlight.</p>
          </div>
        </div>

        <div class="service-box">
          <div class="service-info">
            <h4>social media marketing</h4>
            <p>As a social media marketer, We excel in leveraging digital platforms to amplify brands and drive meaningful engagement. With a strategic blend of creativity and data-driven insights, We craft campaigns that captivate audiences and spark conversations. Let's connect your brand with the right audience and achieve your marketing goals together.</p>
          </div>
        </div>

       </div>
     </section>

     <section class="testimonials" id="testimonials">
      <div class="testimonials-box">
        <h2 class="heading">testimonials</h2>

          <div class="wrapper">
            <div class="testimonial-item">
              <img src="3d-illustration-hipster-guy-with-glasses-brown-jacket.jpg" alt="">
              <h2>person 1</h2>
              <div class="rating">
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
              </div>
              <p>"EBIZCO Marketing Agency has transformed our business. Their innovative strategies and dedication have driven remarkable results. They're not just a service provider; they're a key partner in our success."</p>
            </div>

            <div class="testimonial-item">
              <img src="businesswoman-cartoon-character-gray-background-3d-illustration-business-concept.jpg" alt="">
              <h2>person 2</h2>
              <div class="rating">
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
              </div>
              <p>"Thanks to EBIZCO Marketing Agency, our brand has soared to new heights. Their expertise and dedication have been instrumental in driving our success. Highly recommend!"</p>
            </div>

            <div class="testimonial-item">
              <img src="3d-illustration-cute-boy-with-glasses-white-shirt.jpg" alt="">
              <h2>person 3</h2>
              <div class="rating">
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
                <i class='bx bxs-star' id="star"></i>
              </div>
              <p>"EBIZCO Marketing Agency exceeded our expectations. Their strategic approach and dedication produced tangible results. Highly recommended for anyone seeking impactful marketing solutions."</p>
            </div>

          </div>
        </h2>
      </div>
     </section>

     <section class="contact" id="contact">
      <h2 class="heading">contact <span>me</span></h2>

        <form action="https://formspree.io/f/meqyryzp"
               method="POST">
          
          <div class="input-group">
            <div class="input-box">
              <input type="text" name="name" placeholder="full name">
              <input type="email" name="email" placeholder="email">
            </div>
            <div class="input-box">
              <input type="number" name="phone" placeholder="phone number">
              <input type="text" name="suject" placeholder="subject">
            </div>
          </div>

         <div class="input-group-2">
          <textarea name="message" id="message" cols="30" rows="10" placeholder="your message"></textarea>
          <input type="submit" name="send" value="send message" class="btn">
         </div>

        </form>
     </section>

     <footer class="footer">
      <div class="social">
        <a href="#"><i class="bx bxl-linkedin"></i></a>
          <a href="#"><i class="bx bxl-github"></i></a>
          <a href="#"><i class="bx bxl-instagram-alt"></i></a>
          <a href="#"><i class="bx bxl-twitter"></i></a>
      </div>

      <ul class="list">
        <li>
          <a href="#">faq</a>
        </li>

        <li>
          <a href="#services">services</a>
        </li>

        <li>
          <a href="#">about me</a>
        </li>

        <li>
          <a href="#contact">contact</a>
        </li>

        <li>
          <a href="#testimonials">testimonials</a>
        </li>
      </ul>
       <p class="copyright">
        o saffi ullah | all rights reserved
       </p>
     </footer>

    <script src="script.js"></script>
    <script>
    let menuIcon = document.querySelector('#menu-icon');
let navbar = document.querySelector('.navbar');
let sections = document.querySelectorAll('section');
let navLinks = document.querySelectorAll('header nav a');

window.onscroll = () => {
    sections.forEach(sec => {
        let top = window.scrollY;
        let offset = sec.offsetTop - 150;
        let height = sec.offsetHeight;
        let id = sec.getAttribute('id');

        if(top >= offset && top < offset + height){
            navLinks.forEach(links => {
                links.classList.remove('active');
                document.querySelector('header nav a [href*=' + id + ']').classList.add('active')
            })
        }
    })
}




menuIcon.onclick = () => {
    menuIcon.classList.toggle('bx-x');
    navbar.classList.toggle('active');
}
    </script>
   
  </body>
</html>
