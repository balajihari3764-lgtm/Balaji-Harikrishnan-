<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MR__ Balaji | Student Portfolio</title>
  <style>
    * { margin:0; padding:0; box-sizing:border-box; font-family:Arial, sans-serif; }
    body { line-height:1.6; background:#f9f9f9; color:#333; }

    /* Navbar */
    header { background:#333; color:#fff; padding:1rem; }
    .navbar { display:flex; justify-content:space-between; align-items:center; }
    .nav-links { list-style:none; display:flex; }
    .nav-links li { margin:0 10px; }
    .nav-links a { color:white; text-decoration:none; }

    /* Hero */
    .hero { display:flex; justify-content:center; align-items:center; height:60vh; background:#444; color:white; text-align:center; }
    .hero-content .btn { display:inline-block; margin-top:10px; padding:10px 20px; background:#fff; color:#333; text-decoration:none; border-radius:5px; }

    /* Sections */
    section { padding:2rem; text-align:center; }
    .about-content { display:flex; flex-direction:column; align-items:center; }
    .about-content img { max-width:200px; border-radius:50%; margin-bottom:15px; }

    .project-grid { display:flex; flex-wrap:wrap; gap:1rem; justify-content:center; }
    .project-card { background:#fff; padding:20px; border-radius:10px; width:250px; box-shadow:0 0 10px rgba(0,0,0,0.1); }

    form input, form textarea { width:90%; padding:10px; margin:10px 0; border:1px solid #ccc; border-radius:5px; }
    form button { padding:10px 20px; background:#333; color:#fff; border:none; border-radius:5px; cursor:pointer; }
    form button:hover { background:#555; }

    footer { background:#333; color:white; text-align:center; padding:1rem; margin-top:2rem; }

    /* Quiz App */
    .quiz-container { background:white; padding:20px; border-radius:10px; width:90%; max-width:500px; margin:20px auto; box-shadow:0 0 10px rgba(0,0,0,0.2); }
    .quiz-container ul { list-style:none; text-align:left; }
    .quiz-container li { margin:8px 0; }
    .quiz-container button { margin-top:10px; }

    /* Blog */
    .post { background:white; padding:15px; margin-bottom:20px; border-radius:8px; box-shadow:0 0 5px rgba(0,0,0,0.1); text-align:left; }

    /* Responsive Website */
    .res-header { background:#333; color:#fff; padding:1rem; text-align:center; }
    .res-nav { display:flex; justify-content:center; background:#444; flex-wrap:wrap; }
    .res-nav a { color:white; padding:1rem; text-decoration:none; }
    .res-container { display:grid; grid-template-columns:3fr 1fr; gap:1rem; padding:1rem; }
    .res-content, .res-sidebar { padding:1rem; border-radius:8px; }
    .res-content { background:#f4f4f4; }
    .res-sidebar { background:#e2e2e2; }
    @media(max-width:768px) { .res-container { grid-template-columns:1fr; } }
  </style>
</head>
<body>

  <!-- Navbar -->
  <header>
    <nav class="navbar">
      <div class="logo">MyPortfolio</div>
      <ul class="nav-links" id="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#quiz">Quiz</a></li>
        <li><a href="#blog">Blog</a></li>
        <li><a href="#responsive">Responsive</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <div class="menu-toggle" id="menu-toggle">&#9776;</div>
    </nav>
  </header>

  <!-- Hero -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h1>Hello, I'm <span>MR__ Balaji</span></h1>
      <p>I am the student</p>
      <a href="#projects" class="btn">View My Work</a>
    </div>
  </section>

  <!-- About -->
  <section id="about">
    <h2>About Me</h2>
    <div class="about-content">
      <img src="IMG-20250908-WA0019.jpg" alt="Profile Photo">
      <p>
        I am a student enthusiastic about technology and design.  
        I love building interactive, user-friendly web applications and exploring new tools in the tech world.
      </p>
    </div>
  </section>

  <!-- Projects -->
  <section id="projects">
    <h2>My Projects</h2>
    <div class="project-grid">
      <div class="project-card"><h3>Project 1</h3><p>A simple responsive website.</p></div>
      <div class="project-card"><h3>Project 2</h3><p>JavaScript-based quiz app.</p></div>
      <div class="project-card"><h3>Project 3</h3><p>Personal blog with CMS.</p></div>
    </div>
  </section>

  <!-- Quiz App -->
  <section id="quiz">
    <h2>Simple Quiz App</h2>
    <div class="quiz-container" id="quiz-box">
      <h2 id="question">Question text</h2>
      <ul>
        <li><label><input type="radio" name="answer" class="answer" id="a"> <span id="a_text">Answer A</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="b"> <span id="b_text">Answer B</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="c"> <span id="c_text">Answer C</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="d"> <span id="d_text">Answer D</span></label></li>
      </ul>
      <button id="submit">Submit</button>
      <div class="result" id="result"></div>
    </div>
  </section>

  <!-- Blog -->
  <section id="blog">
    <h2>My Personal Blog</h2>
    <p>Welcome to my personal blog!</p>
    <div id="postsContainer"></div>
  </section>

  <!-- Responsive Website -->
  <section id="responsive">
    <div class="res-header">
      <h1>My Responsive Website</h1>
      <p>Welcome to a simple responsive layout</p>
    </div>
    <nav class="res-nav">
      <a href="#">Home</a><a href="#">About</a><a href="#">Services</a><a href="#">Contact</a>
    </nav>
    <div class="res-container">
      <div class="res-content">
        <h2>Main Content</h2>
        <p>
          This is the main content area. Resize the window to see the responsive effect.  
          On smaller screens, the sidebar will move below the main content.
        </p>
      </div>
      <div class="res-sidebar">
        <h3>Sidebar</h3>
        <p>This is a sidebar with some extra information or links.</p>
      </div>
    </div>
    <p>&copy; 2025 My Website | All Rights Reserved</p>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact Me</h2>
    <form id="contact-form">
      <input type="text" id="name" name="user_name" placeholder="Your Name" required>
      <input type="email" id="email" name="user_email" placeholder="Your Email" required>
      <textarea id="message" name="message" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
    <p id="form-status"></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 MR__ Balaji | All rights reserved</p>
  </footer>

  <script>
    // Quiz Logic
    const quizData = [
      { question:"What does HTML stand for?", a:"Hyper Text Markup Language", b:"High Text Markup Language", c:"Hyperlinks and Text Markup Language", d:"Home Tool Markup Language", correct:"a" },
      { question:"Which language is used for styling web pages?", a:"HTML", b:"JQuery", c:"CSS", d:"XML", correct:"c" },
      { question:"Which is not a JavaScript Framework?", a:"React", b:"Angular", c:"Vue", d:"Django", correct:"d" },
      { question:"Which is used for database?", a:"PHP", b:"MySQL", c:"HTML", d:"CSS", correct:"b" }
    ];
    const questionEl=document.getElementById("question");
    const a_text=document.getElementById("a_text");
    const b_text=document.getElementById("b_text");
    const c_text=document.getElementById("c_text");
    const d_text=document.getElementById("d_text");
    const submitBtn=document.getElementById("submit");
    const resultEl=document.getElementById("result");
    const answerEls=document.querySelectorAll(".answer");

    let currentQuiz=0; let score=0;
    loadQuiz();
    function loadQuiz(){ deselectAnswers(); let q=quizData[currentQuiz]; questionEl.innerText=q.question; a_text.innerText=q.a; b_text.innerText=q.b; c_text.innerText=q.c; d_text.innerText=q.d; }
    function deselectAnswers(){ answerEls.forEach(el=>el.checked=false); }
    function getSelected(){ let ans; answerEls.forEach(el=>{ if(el.checked){ ans=el.id; } }); return ans; }
    submitBtn.addEventListener("click",()=>{ const answer=getSelected(); if(answer){ if(answer===quizData[currentQuiz].correct){ score++; } currentQuiz++; if(currentQuiz<quizData.length){ loadQuiz(); } else { document.getElementById("quiz-box").innerHTML=`<h2>You answered correctly ${score}/${quizData.length} questions.</h2><button onclick="location.reload()">Restart</button>`; } } });

    // Blog load
    function loadPosts() {
      const postsContainer=document.getElementById("postsContainer");
      const posts=JSON.parse(localStorage.getItem("blogPosts")) || [
        {title:"Welcome Post", content:"This is my first blog entry!", date:new Date()}
      ];
      postsContainer.innerHTML="";
      posts.reverse().forEach(post=>{
        const postEl=document.createElement("div");
        postEl.classList.add("post");
        postEl.innerHTML=`<h2>${post.title}</h2><small>${new Date(post.date).toLocaleString()}</small><p>${post.content}</p>`;
        postsContainer.appendChild(postEl);
      });
    }
    loadPosts();
  </script>
</body>
</html>
