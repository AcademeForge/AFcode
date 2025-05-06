<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AST Sample Booklets</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #e0f7fa, #ffffff);
      margin: 0;
      padding: 20px;
      text-align: center;
    }
    h1 {
      color: #00796b;
      font-size: 2.5em;
    }
    .class-btn, .subject-btn, .guest-btn {
      display: inline-block;
      margin: 10px;
      padding: 15px 25px;
      font-size: 1.1em;
      border: none;
      border-radius: 12px;
      background: #4db6ac;
      color: white;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }
    .class-btn:hover, .subject-btn:hover, .guest-btn:hover {
      background: #00796b;
      transform: scale(1.05);
    }
    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <h1>AST Sample Question Booklets</h1>  <div id="class-selection">
    <h2>Select Your Class</h2>
    <div id="class-buttons"></div>
  </div>  <div id="subject-selection" class="hidden">
    <h2>Select Subject</h2>
    <div id="subject-buttons"></div>
  </div>  <div>
    <button class="guest-btn" onclick="alert('Continuing as Guest...')">Continue as Guest</button>
  </div>  <script>
    const subjects = ['English', 'Hindi', 'Math', 'Science', 'General Knowledge'];
    const classButtonsDiv = document.getElementById('class-buttons');
    const subjectButtonsDiv = document.getElementById('subject-buttons');
    const subjectSelectionDiv = document.getElementById('subject-selection');

    for (let i = 1; i <= 10; i++) {
      const btn = document.createElement('button');
      btn.className = 'class-btn';
      btn.textContent = `Class ${i}`;
      btn.onclick = () => showSubjects(i);
      classButtonsDiv.appendChild(btn);
    }

    function showSubjects(selectedClass) {
      subjectButtonsDiv.innerHTML = '';
      subjectSelectionDiv.classList.remove('hidden');

      subjects.forEach(subject => {
        const btn = document.createElement('button');
        btn.className = 'subject-btn';
        btn.textContent = subject;
        btn.onclick = () => {
          const link = `https://drive.google.com/drive/folders/sample-class${selectedClass}-${subject.toLowerCase().replace(/ /g, '-')}`;
          window.open(link, '_blank');
        };
        subjectButtonsDiv.appendChild(btn);
      });
    }
  </script></body>
</html>