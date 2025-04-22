<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Editable Course Schedule</title>
  <style>
    body {
      font-family: Verdana, sans-serif;
      padding: 20px;
      background-color: #f8f9fa;
    }
    h1 {
      color: #b22222;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 20px;
    }
    th, td {
      border: 1px solid #ccc;
      padding: 10px;
      text-align: left;
    }
    th {
      background-color: #f2f2f2;
    }
    input[type="text"] {
      width: 100%;
      box-sizing: border-box;
      padding: 5px;
    }
    .edit-btn {
      padding: 5px 10px;
      margin-top: 5px;
      background-color: #007bff;
      color: white;
      border: none;
      cursor: pointer;
      border-radius: 4px;
    }
    .edit-btn:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>
  <h1>Editable Course Schedule - April 2025</h1>

  <input type="text" id="searchBox" placeholder="Search for a course..." onkeyup="searchCourse()" style="padding:10px;width:300px;margin-bottom:20px;">

  <table id="courseTable">
    <thead>
      <tr>
        <th>Course</th>
        <th>Instructor</th>
        <th>Days</th>
        <th>Time</th>
        <th>Fee</th>
        <th>Room No.</th>
        <th>Actions</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td contenteditable="true">Bharatnatyam</td>
        <td contenteditable="true">Meenakshi Rao</td>
        <td contenteditable="true">Sat & Sun</td>
        <td contenteditable="true">8:30–10:30am</td>
        <td contenteditable="true">₹2800</td>
        <td contenteditable="true">Room 101</td>
        <td><button class="edit-btn" onclick="alert('Changes saved!')">Save</button></td>
      </tr>
      <tr>
        <td contenteditable="true">Tabla</td>
        <td contenteditable="true">Bijoy Mandal</td>
        <td contenteditable="true">Wed & Fri</td>
        <td contenteditable="true">5:00–6:00pm</td>
        <td contenteditable="true">₹2000</td>
        <td contenteditable="true">Room 202</td>
        <td><button class="edit-btn" onclick="alert('Changes saved!')">Save</button></td>
      </tr>
      <tr>
        <td contenteditable="true">Zumba Fitness</td>
        <td contenteditable="true">Shivani</td>
        <td contenteditable="true">Thurs & Sun</td>
        <td contenteditable="true">5:00–6:00pm</td>
        <td contenteditable="true">₹3500</td>
        <td contenteditable="true">Room 303</td>
        <td><button class="edit-btn" onclick="alert('Changes saved!')">Save</button></td>
      </tr>
    </tbody>
  </table>

  <script>
    function searchCourse() {
      let input = document.getElementById("searchBox").value.toLowerCase();
      let rows = document.querySelectorAll("#courseTable tbody tr");

      for (let i = 0; i < rows.length; i++) {
        let rowText = rows[i].innerText.toLowerCase();
        rows[i].style.display = rowText.includes(input) ? "" : "none";
      }
    }
  </script>
</body>
</html>
