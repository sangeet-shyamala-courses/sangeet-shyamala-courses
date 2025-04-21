<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sangeet Shyamala - April 2025 Classes</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f8f9fa;
      margin: 0;
      padding: 20px;
      color: #333;
    }
    h1, h2 {
      color: #b22222;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 40px;
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
      display: table;
    }
  </style>
</head>
<body>
  <h1>Sangeet Shyamala - April 2025 Course Schedule & Fees</h1>

  <input type="text" id="searchBox" placeholder="Search for a course by name..." onkeyup="searchCourses()" />

  <section class="course-table" id="music">
    <h2>Music Classes</h2>
    <table>
      <tr><th>Course</th><th>Instructor</th><th>Days</th><th>Time</th><th>Fee</th><th>Notes</th></tr>
      <tr><td>Hindustani Vocal</td><td>Akansha</td><td>Sat & Sun (Kids)</td><td>10:00–11:00 AM</td><td>₹3000/month</td><td>₹1200/hour (Individual)</td></tr>
      <tr><td>Piano & Voice</td><td>Kinneret Prabhudas</td><td>Mon to Thurs</td><td>9:00 AM – 6:45 PM</td><td>₹2000 (45 min), ₹1500 (30 min)</td><td>Individual</td></tr>
      <tr><td>Tabla</td><td>Bijoy Mandal</td><td>Wed, Fri & Sat</td><td>Varies</td><td>₹2000–₹4500/month</td><td>Age 4+</td></tr>
      <tr><td>Vocal & Sitar</td><td>Sephali Maiti</td><td>Tues & Fri</td><td>5:00–6:00 PM</td><td>₹2000/month</td><td></td></tr>
      <tr><td>Sitar (Group)</td><td>—</td><td>Tues</td><td>4:00–5:00 PM</td><td>₹4000/month</td><td>₹1500/class (Individual)</td></tr>
    </table>
  </section>

  <section class="course-table" id="dance">
    <h2>Dance Classes</h2>
    <table>
      <tr><th>Course</th><th>Instructor</th><th>Days</th><th>Time</th><th>Fee</th><th>Notes</th></tr>
      <tr><td>Bharatnatyam</td><td>Meenakshi Rao</td><td>Sat & Sun</td><td>8:30–12:00 PM</td><td>₹2800 (8 classes)</td><td>Multiple Batches</td></tr>
      <tr><td>Kathak</td><td>Deepti Gupta</td><td>Multiple Days</td><td>Varies</td><td>₹2000–₹2300 (8 classes)</td><td>Beginner & Advanced</td></tr>
      <tr><td>Ballet</td><td>Komal</td><td>Thurs & Sat</td><td>4:00–5:00 PM</td><td>₹3000 (4), ₹5500 (8)</td><td>Age 4+</td></tr>
      <tr><td>Odissi</td><td>Subrata Tripathy</td><td>Thursday</td><td>3:30–5:00 PM</td><td>₹2000 (4 classes)</td><td>Age 4+</td></tr>
      <tr><td>Dance Fitness</td><td>Ajay Soni</td><td>Mon, Wed, Fri</td><td>6:15–7:15 PM</td><td>₹3500 (8), ₹4500 (12)</td><td></td></tr>
      <tr><td>Zumba Fitness</td><td>Shivani</td><td>Thurs, Sat, Sun</td><td>Various</td><td>₹2000 (4), ₹3500 (8)</td><td>Ages 3.5+ and 8+</td></tr>
    </table>
  </section>

  <section class="course-table" id="fitness">
    <h2>Fitness</h2>
    <table>
      <tr><th>Course</th><th>Instructor</th><th>Days</th><th>Time</th><th>Fee</th><th>Notes</th></tr>
      <tr><td>Yoga</td><td>—</td><td>Tues & Thurs</td><td>6:00–7:00 PM</td><td>₹3000 (8 classes)</td><td></td></tr>
      <tr><td>Karate</td><td>Tarun Chakravarty</td><td>Mon & Thurs</td><td>5:00–6:00 PM</td><td>₹2000 (8 classes)</td><td></td></tr>
    </table>
  </section>

  <section class="course-table" id="art">
    <h2>Art Classes</h2>
    <table>
      <tr><th>Course</th><th>Instructor</th><th>Days</th><th>Time</th><th>Fee</th><th>Notes</th></tr>
      <tr><td>Painting</td><td>Gaurav Nagar</td><td>Tues, Thurs, Sun</td><td>11:00–1:00, 4:00–6:00</td><td>₹2000 (4), ₹4200 (12), ₹700/hr</td><td>Individual and Group</td></tr>
      <tr><td>Sculpture</td><td>Javed Hussain</td><td>Sat & Sun</td><td>10:30–12:30 PM</td><td>₹2500 (8 classes)</td><td></td></tr>
    </table>
  </section>

  <section class="course-table" id="writing">
    <h2>Creative Writing</h2>
    <table>
      <tr><th>Instructor</th><th>Days</th><th>Time</th><th>Fee</th><th>Notes</th></tr>
      <tr><td>Kiran Mishra</td><td>Sat & Sun</td><td>Sat: 11–12, Sun: 3–4</td><td>₹2000 (4 classes), ₹700/hr (Individual)</td><td></td></tr>
    </table>
  </section>

  <script>
    function searchCourses() {
      const input = document.getElementById("searchBox").value.toLowerCase();
      const sections = document.querySelectorAll(".course-table");
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
  </script>
</body>
</html>
