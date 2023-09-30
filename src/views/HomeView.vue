<script setup>
import TheWelcome from '../components/TheWelcome.vue'
</script>

<template>
  <main>
    <section id="profile">
      <div class="prof_pic">
        <img class="prof" src="../assets/rayul-_M6gy9oHgII-unsplash.jpg" alt="">
      </div>
      <div class="section_text">
        <h1 class="title">Hi, I'm Yasi and I am a experienced <span class="title" style="text-decoration: underline;">graphic designer</span> and <span class="title" style="color: rgb(33, 33, 33);">web developer</span></h1>
        <p>Create designs that express your brand</p>
      </div>
    </section>
    <section>
      <div class="about-box">
        <div class="about-left">
          <h2 class="about-title">PERSONAL INFO</h2>
          <div class="about-left-text">
            <p style="color: rgb(193, 193, 193);">
              Hi, I'm Yasi Kulathunga, based in Geelong-Australia,
              I am a experienced graphic designer and web developer 
              specialized in creating stunnig social media and web designs. 
            </p>

            <ul class="about-socials">
              <li class="web-li">
                <a href="https://github.com/YasithKulathunga" target="blank">Github</a>
              </li>
              <li class="web-li">
                <a href="www.hardydesigns@studio">website</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="about-right">
          <h2 class="about-title">SKILLS</h2>
          <div class="skill-right">
            <ul class="skills-list">
              <li>HTML</li>
              <li>CSS</li>
              <li>Javascript</li>
              <li>Vue 3</li>
              <li>Photoshop</li>
              <li>Figma</li>
            </ul>
          </div>
        </div>
      </div>
    </section>
    <section class="education">
      <h2 class="about-title">Education</h2>

      <h1>Bachelor in Information Technology</h1>
      <div>
        <span>Deakin University - Waurn Ponds</span><br>
        <span>2023 - 2026</span>
      </div>
      
      <h1>Master in Web Development</h1>
      <div>
        <span>Deakin University - Waurn Ponds</span><br>
        <span>2027 - 2029</span>
      </div>

      <h1>Photoshop/Illustratior</h1>
      <div>
        <span>Skill Share/ Self taught</span><br>
        <span>2018 - </span>
      </div>

      <h1>Still learning</h1>
      <div>
        <span>On my own </span><br>
        <span>since 2002</span>
      </div>

    
    </section>
    <section class="services">
      <h1 style="text-align: center; margin-bottom: 30px;" class="title">i am specialized in..</h1>
      <div class="services-list">
        <div class="sev-box"><h3>Posters</h3></div>
        <div class="sev-box"><h3>App and Web <br> Development</h3></div>
        <div class="sev-box"><h3>Products</h3></div>
      </div>
    </section>
  </main>

</template>

<style>

.education{
  text-align: right;
}

.about-box{
    display: flex;
    justify-content: center;
    color: white;
    border-radius: 50px;
    background-color: rgb(31, 31, 31);
}

.about-left{
    flex-basis: 60%;
    padding: 40px;
}

.about-right{
  margin-left: 200px;
  flex-basis: 20% ;
  padding: 40px;
}


.about-title{
  text-decoration: underline;
  font-size: 2rem;
  margin-bottom: 20px;
}
.about-socials{
  display: flex;
  column-gap: 1rem;
}

h1{
  margin-top: 20px;
}
.skills-list{
  font-size: 20px;
}

.web-li{
  list-style: none;
}


p{
  margin-bottom: 10px;
  text-align: justify;
  text-justify: inter-word;
}

a{
  color: rgb(252, 252, 252);
  text-decoration: none;
  font-size: 20px;
}


.services-list{
  display: flex;
  align-items: center;
  justify-content: center;
}

.sev-box{
  width: 100px;
  height: 500px;
  margin: 10px;
  border-radius: 50px;
  background: url(https://images.unsplash.com/photo-1511466431307-d603e868975c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fHBvc3RlcnN8ZW58MHx8MHx8fDA%3D&auto=format&fit=crop&w=1200&q=60);
  background-size: cover;
  background-position: center;
  position: relative;
  transition: width 0.5s;
}

.sev-box:nth-child(2){
  background-image: url(https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NHx8YXBwJTIwZGVzaWdufGVufDB8fDB8fHww&auto=format&fit=crop&w=1200&q=60);
  background-size: cover;
  background-position: center;
}

.sev-box:nth-child(3){
  background-image: url(https://images.unsplash.com/photo-1611930022073-b7a4ba5fcccd?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80);
  background-size: cover;
  background-position: center;
}

.sev-box h3{
  color: rgb(0, 0, 0);
  position: absolute;
  bottom: 0;
  left: 30px;
  opacity: 0;
  transition: bottom 0.5s, opacity 0.5s;
}

.sev-box:hover{
  width: 300px;
  cursor: pointer;
}

.sev-box:hover h3{
  opacity: 1;
  bottom: 25px;
} 



p{
  text-align: left;
  font-size: 30px;
  color: rgb(144, 144, 144);
}
.prof{
  border-radius: 300px;
}
</style>
