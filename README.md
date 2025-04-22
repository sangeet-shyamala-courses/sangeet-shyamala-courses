<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sangeet Shyamala - April 2025 Classes</title>
  <style>
    :root {
      --font-family: Arial;
      --bg-color: #f8f9fa;
      --text-color: #333;
      --highlight-color: #b22222;
    }

    body {
      font-family: var(--font-family), sans-serif;
      background-color: var(--bg-color);
      margin: 0;
      padding: 20px;
      color: var(--text-color);
    }

    h1, h2 {
      color: var(--highlight-color);
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 40px;
      overflow-x: auto;
      display: block;
    }

    th, td {
      border: 1px solid #ccc;
      padding: 10px;
      text-align: left;
    }

    th {
      background-color: #f2f2f2;
    }

    section {
      margin-bottom: 50px;
    }

    #searchBox {
      padding: 10px;
      width: 100%;
      max-width: 400px;
      margin: 20px 0;
      font-size: 16px;
    }

    .course-table {
      display: none;
    }

    .visible {
      display: block;
      border: 2px solid var(--highlight-color);
      box-shadow: 0 0 10px rgba(178, 34, 34, 0.4);
      border-radius: 10px;
    }

    #logo {
      width: 150px;
      height: auto;
      margin-bottom: 20px;
    }

    .teacher-image {
      width: 100px;
      height: auto;
      border-radius: 10px;
      margin-top: 10px;
    }

    #settings {
      margin-bottom: 20px;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 10px;
      background-color: #fff;
    }

    #settings label {
      margin-right: 10px;
    }

    @media (max-width: 768px) {
      table, th, td {
        font-size: 14px;
      }

      #searchBox, #bgColorPicker, #fontPicker, #themeSelector {
        font-size: 14px;
        width: 100%;
      }

      h1 {
        font-size: 22px;
      }

      h2 {
        font-size: 18px;
      }

      #logo {
        width: 120px;
      }
    }

    @media (max-width: 480px) {
      body {
        padding: 10px;
      }

      #searchBox, #bgColorPicker, #fontPicker, #themeSelector {
        width: 100%;
        font-size: 12px;
      }

      h1 {
        font-size: 20px;
      }

      h2 {
        font-size: 16px;
      }
    }

    .highlighted {
      background-color: #ffeb3b; /* Yellow highlight */
    }

  </style>
</head>
<body>
  <img id="logo" src="" alt="Sangeet Shyamala Logo" onerror="this.style.display='none'" />
  <h1>Sangeet Shyamala - April 2025 Course Schedule & Fees</h1>

  <div id="settings">
    <label>Upload Logo: <input type="file" accept="image/*" onchange="uploadLogo(event)" /></label><br>
    <label>Background Color: <input type="color" id="bgColorPicker" onchange="changeBackgroundColor()" /></label><br>
    <label>Font Style:
      <select id="fontPicker" onchange="changeFontFamily()">
        <option value="Arial">Arial</option>
        <option value="Verdana">Verdana</option>
        <option value="Georgia">Georgia</option>
        <option value="Times New Roman">Times New Roman</option>
        <option value="Courier New">Courier New</option>
      </select>
    </label><br>
    <label>Theme:
      <select id="themeSelector" onchange="changeTheme()">
        <option value="light">Light</option>
        <option value="dark">Dark</option>
        <option value="classic">Classic</option>
      </select>
    </label><br>
    <label>Upload Teacher Image: <input type="file" accept="image/*" onchange="uploadTeacherImage(event)" /></label><br>
    <div id="teacherImagePreview"></div>
  </div>

  <input type="text" id="searchBox" placeholder="Search for a course by name..." onkeyup="searchCourses()" />

  <section class="course-table visible">
    <h2>Full Course List - April 2025</h2>
    <div style="white-space: pre-wrap; font-size: 14px">
      <div id="danceFitness" class="course">
        <strong>Dance Fitness – Ajay Soni</strong><br>
        Days: Mon, Wed, Fri<br>
        Timings: 6:15 to 7:15pm<br>
        Fee: ₹3500 (8 classes), ₹4500 (12 classes)<br><br>
      </div>

      <div id="zumbaFitness" class="course">
        <strong>Zumba Fitness – Shivani</strong><br>
        Days: Thurs & Sat, Sun<br>
        Timings: 12:30–1:30pm (Sun - Bgnr), 5:00–6:00pm (Thurs & Sat)<br>
        Fee: ₹2000 (4 classes), ₹3500 (8 classes)<br><br>
      </div>

      <div id="yoga" class="course">
        <strong>Yoga – Geetika</strong><br>
        Days: Tues & Thurs<br>
        Timings: 6:00 to 7:00pm<br>
        Fee: ₹3000 (8 classes)<br><br>
      </div>

      <div id="karate" class="course">
        <strong>Karate – Tarun Chakravarty</strong><br>
        Days: Mon & Thurs<br>
        Timings: 5:00 to 6:00pm<br>
        Fee: ₹2000 (8 classes)<br><br>
      </div>

      <div id="contemporaryDance" class="course">
        <strong>Contemporary Dance – Shivani</strong><br>
        Days: Wed & Fri<br>
        Timings: 4:00–5:00pm<br>
        Fee: ₹3500 (8 classes)<br>
      </div>
    </div>
  </section>

  <script>
    function searchCourses() {
      const input = document.getElementById("searchBox").value.toLowerCase();
      const sections = document.querySelectorAll(".course");
      let found = false;

      sections.forEach(section => {
        const text = section.innerText.toLowerCase();
        if (text.includes(input) && input !== "") {
          section.classList.add("visible");
          found = true;
        } else {
          section.classList.remove("visible");
        }
      });

      if (!found && input !== "") {
        alert("No matching course found. Try a different keyword.");
      } else if (input === "") {
        sections.forEach(section => section.classList.remove("visible"));
      }
    }

    function uploadLogo(event) {
      const file = event.target.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function(e) {
          document.getElementById("logo").src = e.target.result;
        }
        reader.readAsDataURL(file);
      }
    }

    function uploadTeacherImage(event) {
      const file = event.target.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function(e) {
          const img = document.createElement("img");
          img.src = e.target.result;
          img.className = "teacher-image";
          document.getElementById("teacherImagePreview").innerHTML = "";
          document.getElementById("teacherImagePreview").appendChild(img);
        }
        reader.readAsDataURL(file);
      }
    }

    function changeBackgroundColor() {
      const color = document.getElementById("bgColorPicker").value;
      document.body.style.setProperty("--bg-color", color);
    }

    function changeFontFamily() {
      const font = document.getElementById("fontPicker").value;
      document.body.style.setProperty("--font-family", font);
    }

    function changeTheme() {
      const theme = document.getElementById("themeSelector").value;
      if (theme === "light") {
        document.body.style.setProperty("--bg-color", "#f8f9fa");
        document.body.style.setProperty("--text-color", "#333");
        document.body.style.setProperty("--highlight-color", "#b22222");
      } else if (theme === "dark") {
        document.body.style.setProperty("--bg-color", "#1e1e1e");
        document.body.style.setProperty("--text-color", "#f0f0f0");
        document.body.style.setProperty("--highlight-color", "#ff6347");
      } else if (theme === "classic") {
        document.body.style.setProperty("--bg-color", "#fff8dc");
        document.body.style.setProperty("--text-color", "#000080");
        document.body.style.setProperty("--highlight-color", "#8b0000");
      }
    }

    // Function to highlight a row when clicked
    document.querySelectorAll('.course').forEach(item => {
      item.addEventListener('click', function() {
        document.querySelectorAll('.course').forEach(course => {
          course.classList.remove('highlighted');
        });
        item.classList.add('highlighted');
      });
    });
  </script>
</body>
</html>
