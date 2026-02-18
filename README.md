<div align="center">

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Banner</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=DM+Sans:wght@300;400&display=swap" rel="stylesheet">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: #0d0d1a;
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
  }

  .banner {
    width: 100%;
    max-width: 900px;
    position: relative;
    overflow: hidden;
    border-radius: 0;
  }

  /* SVG WAVE CONTAINER */
  .banner svg.wave-top {
    display: block;
    width: 100%;
  }

  /* MAIN BODY */
  .banner-body {
    background: linear-gradient(135deg, #0d0d1a 0%, #1e1b4b 50%, #4f46e5 100%);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 3rem 2rem 2rem;
    position: relative;
    overflow: hidden;
  }

  /* Animated particles */
  .banner-body::before {
    content: '';
    position: absolute;
    width: 400px; height: 400px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(99,102,241,0.25) 0%, transparent 70%);
    top: -100px; right: -80px;
    animation: floatA 8s ease-in-out infinite;
  }
  .banner-body::after {
    content: '';
    position: absolute;
    width: 300px; height: 300px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(139,92,246,0.2) 0%, transparent 70%);
    bottom: -80px; left: -60px;
    animation: floatB 10s ease-in-out infinite;
  }

  @keyframes floatA {
    0%,100% { transform: translate(0,0) scale(1); }
    50% { transform: translate(-30px, 20px) scale(1.1); }
  }
  @keyframes floatB {
    0%,100% { transform: translate(0,0) scale(1); }
    50% { transform: translate(20px, -25px) scale(1.08); }
  }

  /* Floating dots */
  .dot {
    position: absolute;
    border-radius: 50%;
    background: rgba(255,255,255,0.15);
    animation: drift linear infinite;
  }
  .dot:nth-child(1)  { width:4px;  height:4px;  top:20%; left:10%; animation-duration:12s; animation-delay:0s; }
  .dot:nth-child(2)  { width:6px;  height:6px;  top:60%; left:20%; animation-duration:18s; animation-delay:2s; }
  .dot:nth-child(3)  { width:3px;  height:3px;  top:35%; left:75%; animation-duration:14s; animation-delay:4s; }
  .dot:nth-child(4)  { width:5px;  height:5px;  top:75%; left:85%; animation-duration:16s; animation-delay:1s; }
  .dot:nth-child(5)  { width:4px;  height:4px;  top:15%; left:55%; animation-duration:20s; animation-delay:3s; }
  .dot:nth-child(6)  { width:7px;  height:7px;  top:50%; left:45%; animation-duration:22s; animation-delay:5s; }

  @keyframes drift {
    0%   { transform: translateY(0px) rotate(0deg); opacity: 0.4; }
    50%  { transform: translateY(-40px) rotate(180deg); opacity: 0.8; }
    100% { transform: translateY(0px) rotate(360deg); opacity: 0.4; }
  }

  /* TEXT */
  .banner-content {
    position: relative;
    z-index: 2;
    text-align: center;
  }

  .greeting {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2.2rem, 5vw, 3.6rem);
    font-weight: 800;
    color: #ffffff;
    letter-spacing: -0.02em;
    line-height: 1.1;
    animation: fadeSlideDown 0.9s cubic-bezier(.22,1,.36,1) both;
  }

  .wave-emoji {
    display: inline-block;
    animation: wave 2.2s ease-in-out infinite;
    transform-origin: 70% 80%;
  }

  @keyframes wave {
    0%,60%,100% { transform: rotate(0deg); }
    10%,30% { transform: rotate(18deg); }
    20% { transform: rotate(-8deg); }
    40% { transform: rotate(12deg); }
    50% { transform: rotate(-4deg); }
  }

  .tagline {
    font-family: 'DM Sans', sans-serif;
    font-size: clamp(0.95rem, 2vw, 1.15rem);
    font-weight: 300;
    color: rgba(255,255,255,0.75);
    margin-top: 0.9rem;
    letter-spacing: 0.02em;
    animation: fadeSlideDown 0.9s 0.2s cubic-bezier(.22,1,.36,1) both;
  }

  /* Accent line */
  .accent-line {
    width: 60px;
    height: 3px;
    background: linear-gradient(90deg, #818cf8, #a78bfa);
    border-radius: 2px;
    margin: 1.2rem auto 0;
    animation: expandLine 1s 0.5s ease both;
  }
  @keyframes expandLine {
    from { width: 0; opacity: 0; }
    to   { width: 60px; opacity: 1; }
  }

  @keyframes fadeSlideDown {
    from { opacity: 0; transform: translateY(-16px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* BOTTOM WAVE */
  .wave-bottom {
    display: block;
    width: 100%;
    background: linear-gradient(135deg, #0d0d1a 0%, #1e1b4b 50%, #4f46e5 100%);
  }
</style>
</head>
<body>

<div class="banner">

  <!-- TOP WAVE -->
  <svg class="wave-top" viewBox="0 0 1200 60" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <linearGradient id="topGrad" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%"   stop-color="#0d0d1a"/>
        <stop offset="50%"  stop-color="#1e1b4b"/>
        <stop offset="100%" stop-color="#4f46e5"/>
      </linearGradient>
    </defs>
    <path d="M0,0 L1200,0 L1200,20 Q1050,60 900,35 Q750,10 600,40 Q450,65 300,30 Q150,0 0,45 Z" fill="url(#topGrad)"/>
  </svg>

  <!-- MAIN CONTENT -->
  <div class="banner-body">
    <!-- floating dots -->
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot"></div>
    <div class="dot"></div>

    <div class="banner-content">
      <div class="greeting">Hey, I'm Tharusha <span class="wave-emoji">👋</span></div>
      <div class="tagline">I build things for the web, mobile &amp; beyond</div>
      <div class="accent-line"></div>
    </div>
  </div>

  <!-- BOTTOM WAVE -->
  <svg class="wave-bottom" viewBox="0 0 1200 60" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <linearGradient id="botGrad" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%"   stop-color="#4f46e5"/>
        <stop offset="50%"  stop-color="#1e1b4b"/>
        <stop offset="100%" stop-color="#0d0d1a"/>
      </linearGradient>
    </defs>
    <path d="M0,60 L1200,60 L1200,15 Q1050,0 900,30 Q750,55 600,20 Q450,-5 300,35 Q150,60 0,20 Z" fill="url(#botGrad)"/>
  </svg>

</div>

</body>
</html>

</div>

<br/>

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=18&pause=1000&color=818CF8&center=true&vCenter=true&width=700&lines=Software+Engineering+Undergraduate+%40+UoM+%F0%9F%87%B1%F0%9F%87%B0;Full+Stack+Developer+%7C+Angular+%2B+ASP.NET+%7C+React+%2B+Node;Embedded+Systems+%26+IoT+Enthusiast;Building+real+software+that+solves+real+problems+%F0%9F%9A%80)](https://git.io/typing-svg)

</div>

---

<img align="right" width="360" src="https://github-readme-stats.vercel.app/api?username=Tharusha-Rayan&show_icons=true&theme=tokyonight&hide_border=true&border_radius=16&count_private=true&title_color=818cf8&icon_color=6366f1&text_color=c7d2fe&bg_color=0d0d1a"/>

### 👨‍💻 Who am I?

I'm **Tharusha Rayan**, a Software Engineering undergraduate at the **University of Moratuwa, Sri Lanka** 🇱🇰

I love turning complex problems into clean, scalable software. My sweet spot is **full-stack web development** — from crafting smooth UIs to designing robust backend APIs and databases.

When I'm not writing code, you'll find me tinkering with **embedded systems & IoT**, mentoring fellow students in robotics, or exploring new tools and frameworks.

```yaml
name:       Tharusha Rayan
university: University of Moratuwa 🇱🇰
degree:     BSc (Hons) Information Technology
focus:      Full Stack Development
currently:  Building enterprise & open-source projects
```

<br clear="right"/>

---

### 🔥 What I Do

<table>
  <tr>
    <td align="center" width="33%">
      <img src="https://img.shields.io/badge/-Frontend-1e1b4b?style=for-the-badge" /><br/><br/>
      <b>Frontend Development</b><br/>
      <sub>Angular · React · Flutter<br/>Responsive, fast & clean UIs</sub>
    </td>
    <td align="center" width="33%">
      <img src="https://img.shields.io/badge/-Backend-1e1b4b?style=for-the-badge" /><br/><br/>
      <b>Backend Development</b><br/>
      <sub>ASP.NET Core · Spring Boot · Node.js<br/>REST APIs · Enterprise systems</sub>
    </td>
    <td align="center" width="33%">
      <img src="https://img.shields.io/badge/-Embedded-1e1b4b?style=for-the-badge" /><br/><br/>
      <b>Embedded & IoT</b><br/>
      <sub>C / C++ · Arduino </sub>
    </td>
  </tr>
</table>

---

### 🛠️ Tech Stack

**Languages**

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)

**Frontend**

![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

**Backend**

![ASP.NET Core](https://img.shields.io/badge/ASP.NET_Core-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge&logo=express&logoColor=white)

**Databases**

![MSSQL](https://img.shields.io/badge/MSSQL-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

**Tools & Platforms**

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)

---

### 🚀 Featured Projects

<table>
<tr>
<td width="50%" valign="top">

#### 🏭 Tea Factory Supply Chain Management
Enterprise web & mobile system — digitizing green leaf collection, inventory, payments & reporting across a full factory supply chain.

> 💡 **My role:** Transportation module with Google Maps route tracking & cost analytics

![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![MSSQL](https://img.shields.io/badge/MSSQL-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)

[![View](https://img.shields.io/badge/View_Repo_%E2%86%92-181717?style=for-the-badge&logo=github)](https://github.com/TharinduMahesh/TFSMS_NextGenNerds)

</td>
<td width="50%" valign="top">

#### 🛒 ShopMart — E-Commerce Platform
Full-stack marketplace for buyers & sellers with secure authentication, real-time order tracking, refund management & email notifications.

&nbsp;

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-404D59?style=flat-square&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

[![View](https://img.shields.io/badge/View_Repo_%E2%86%92-181717?style=for-the-badge&logo=github)](https://github.com/Tharusha-Rayan/ShopMart)

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 🚗 Autocare 360 — Vehicle Service Management
Automated service booking & customer tracking for vehicle maintenance. Appointment scheduling meets smart customer notifications.

> 💡 **My role:** Chatbot support system & real-time notifications

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

[![View](https://img.shields.io/badge/View_Repo_%E2%86%92-181717?style=for-the-badge&logo=github)](https://github.com/Chamithjay/auto_service_frontend)

</td>
<td width="50%" valign="top">

#### 🎓 EduLearn — E-Learning Platform
Digital course delivery platform with structured learning paths, interactive quizzes, progress tracking & automated certificate generation.

&nbsp;

![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![MSSQL](https://img.shields.io/badge/MSSQL-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)

[![View](https://img.shields.io/badge/View_Repo_%E2%86%92-181717?style=for-the-badge&logo=github)](https://github.com/Tharusha-Rayan/E-Learning-System)

</td>
</tr>
</table>

---

### 📈 GitHub Activity

<div align="center">

<img src="https://streak-stats.demolab.com?user=Tharusha-Rayan&theme=tokyonight&hide_border=true&border_radius=14&ring=6366f1&fire=818cf8&currStreakLabel=818cf8&sideLabels=818cf8" width="49%"/>
&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Tharusha-Rayan&theme=tokyonight&hide_border=true&border_radius=14&layout=compact&langs_count=8&title_color=818cf8" width="38%"/>

<br/><br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Tharusha-Rayan&theme=tokyo-night&hide_border=true&radius=14&area=true&line=6366f1&point=818cf8&area_color=4f46e5" width="97%"/>

</div>

---

### 🤝 Let's Connect

<div align="center">

I'm always open to interesting projects, collaborations, or just a good tech conversation ☕

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-6366f1?style=for-the-badge&logo=google-chrome&logoColor=white)](#)
[![Email](https://img.shields.io/badge/Email-Say_Hi-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your@email.com)

<br/>

![Profile Views](https://komarev.com/ghpvc/?username=Tharusha-Rayan&style=for-the-badge&color=6366f1&label=PROFILE+VIEWS)

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:4f46e5,50:1e1b4b,100:0d0d1a&height=120&section=footer" width="100%"/>

</div>
