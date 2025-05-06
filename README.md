<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AST Sample Booklets</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #e3f2fd, #ffffff);
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      overflow: hidden;
      text-align: center;
    }h1, h2 {
  color: #0d47a1;
  animation: fadeIn 1.5s ease-in-out;
}

p {
  max-width: 600px;
  margin: 10px auto;
  color: #37474f;
  font-size: 1.1em;
}

.btn {
  display: inline-block;
  margin: 10px;
  padding: 15px 30px;
  font-size: 1.2em;
  border: none;
  border-radius: 16px;
  background: linear-gradient(to right, #42a5f5, #1e88e5);
  color: white;
  cursor: pointer;
  transition: all 0.4s ease;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

.btn:hover {
  background: linear-gradient(to right, #1e88e5, #1565c0);
  transform: scale(1.1);
}

.hidden {
  display: none;
}

@keyframes fadeIn {
  0% {opacity: 0; transform: translateY(-20px);}
  100% {opacity: 1; transform: translateY(0);}
}

.back-btn {
  background: linear-gradient(to right, #ef5350, #e53935);
}

.back-btn:hover {
  background: linear-gradient(to right, #e53935, #b71c1c);
}

  </style>
</head>
<body>
  <div id="login-view">
    <h1>Welcome to AcademeForge</h1>
    <p><strong>AcademeForge</strong> is a student-centric platform committed to revolutionizing the education system for Classes 1 to 12 in India. Our mission is to make learning exciting, practical, and accessible for every student.</p>
    <p>The <strong>AcademeForge Scholars Test (AST)</strong> is a multi-round assessment program that encourages students to test their knowledge, challenge themselves, and earn recognition and scholarships. This portal allows you to access free sample questions curated for Class 1 to 10, across all major subjects.</p>
    <button class="btn" onclick="showClassView()">Continue as Guest</button>
  </div>  <div id="class-view" class="hidden">
    <h2>Select Your Class</h2>
    <div id="class-buttons"></div>
    <button class="btn back-btn" onclick="goBackToLogin()">Back</button>
  </div>  <div id="subject-view" class="hidden">
    <h2>Select Subject</h2>
    <div id="subject-buttons"></div>
    <button class="btn back-btn" onclick="goBackToClassView()">Back</button>
  </div>  <script>
    const driveLinks = {
      1: {
        English: 'https://drive.google.com/drive/folders/1W299Qrb3dBchYz2DJkjGXn1WAv7hBEkz',
        Hindi: 'https://drive.google.com/drive/folders/1W1uFIcFyDH8v6wof4Azw-tNDwnKJOn60',
        Math: 'https://drive.google.com/drive/folders/1W2AaOKE-XMxmW-g9XNodpF_KMo96SIN9',
        Science: 'https://drive.google.com/drive/folders/1W2LPRDGmJHnxmynPt0iiT8Ycg2DrIjkR',
        'General Knowledge': 'https://drive.google.com/drive/folders/1W59dvNw0yRuuKQJr7-yR_1_vx1TguIZ4'
      },
      2: {
        English: 'https://drive.google.com/drive/folders/1X7DrAzxznFNI2_zDTVuGVbrzv1cPm2Py',
        Hindi: 'https://drive.google.com/drive/folders/1XCRDs0esylsvg3xIwKdRJlN569Ev649D',
        Math: 'https://drive.google.com/drive/folders/1XDLd2yvwz_Ynia4pOE_T2UTt4w8zGH1i',
        Science: 'https://drive.google.com/drive/folders/1XEDPwWL_SjSZrXiRr1IuaQO6oD59c5Tp',
        'General Knowledge': 'https://drive.google.com/drive/folders/1X_Q47wncULapX0wxQ0rqcp2bxMV-Ekd8'
      },
      3: {
        English: 'https://drive.google.com/drive/folders/1Xckw43MJuUDfMEEwsz_Yd1oMo5YI_Cgk',
        Hindi: 'https://drive.google.com/drive/folders/1XkjEC6Z7dcECjGh7gGOQzjgdYyxJxhbu',
        Math: 'https://drive.google.com/drive/folders/1XoAhslwjJUqjKHMDan0OffIm3tQ8pLl7',
        Science: 'https://drive.google.com/drive/folders/1XqJaCpmgQJTBzU4nlAKIqR4QHoTCrpWy',
        'General Knowledge': 'https://drive.google.com/drive/folders/1XzDGc1fGhgvFRtIGHx6lvPCvW2_IRtbG'
      },
      4: {
        English: 'https://drive.google.com/drive/folders/1Y1XnZqOtfVqSryrwd3zxtxiI5qjBoATu',
        Hindi: 'https://drive.google.com/drive/folders/1YCNgdg1OLswVzDhl_15v7Q4eypaJQ4DH',
        Math: 'https://drive.google.com/drive/folders/1YGbFjminjVGFEenNruBJjzISyKWQ_UOw',
        Science: 'https://drive.google.com/drive/folders/1YId70S0nDgLB-blB9NiFxUl1KkhtboOl',
        'General Knowledge': 'https://drive.google.com/drive/folders/1YSSmD3qZfTScdAXHv7OErpKADKVRFnI-'
      },
      5: {
        English: '#',
        Hindi: '#',
        Math: '#',
        Science: '#',
        'General Knowledge': '#'
      },
      6: {
        English: '#',
        Hindi: '#',
        Math: '#',
        Science: '#',
        'General Knowledge': '#'
      },
      7: {
        English: '#',
        Hindi: '#',
        Math: '#',
        Science: '#',
        'General Knowledge': '#'
      },
      8: {
        English: '#',
        Hindi: '#',
        Math: '#',
        Science: '#',
        'General Knowledge': '#'
      },
      9: {
        English: '#',
        Hindi: '#',
        Math: '#',
        Science: '#',
        'General Knowledge': '#'
      },
      10: {
        English: '#',
        Hindi: '#',
        Math: '#',
        Science: '#',
        'General Knowledge': '#'
      }
    };

    let selectedClass = null;

    function showClassView() {
      document.getElementById('login-view').classList.add('hidden');
      document.getElementById('class-view').classList.remove('hidden');

      const classButtons = document.getElementById('class-buttons');
      classButtons.innerHTML = '';
      for (let i = 1; i <= 10; i++) {
        const btn = document.createElement('button');
        btn.className = 'btn';
        btn.textContent = `Class ${i}`;
        btn.onclick = () => showSubjectView(i);
        classButtons.appendChild(btn);
      }
    }

    function showSubjectView(classNum) {
      selectedClass = classNum;
      document.getElementById('class-view').classList.add('hidden');
      document.getElementById('subject-view').classList.remove('hidden');

      const subjectButtons = document.getElementById('subject-buttons');
      subjectButtons.innerHTML = '';
      const subjects = ['English', 'Hindi', 'Math', 'Science', 'General Knowledge'];

      subjects.forEach(subject => {
        const btn = document.createElement('button');
        btn.className = 'btn';
        btn.textContent = subject;
        btn.onclick = () => {
          const link = driveLinks[classNum]?.[subject];
          if (link && link !== '#') {
            window.open(link, '_blank');
          } else {
            alert('Link will be available soon for all subjects, stay tuned.');
          }
        };
        subjectButtons.appendChild(btn);
      });
    }

    function goBackToLogin() {
      document.getElementById('class-view').classList.add('hidden');
      document.getElementById('login-view').classList.remove('hidden');
    }

    function goBackToClassView() {
      document.getElementById('subject-view').classList.add('hidden');
      document.getElementById('class-view').classList.remove('hidden');
    }
  </script></body>
</html>