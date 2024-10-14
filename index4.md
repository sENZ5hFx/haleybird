<!DOCTYPE html>
<html>
<head>
  <title>Haley Bird - Interactive Resume</title>
  <style>
    /* CSS Styling - You can customize this to match your desired theme */
    .skill-container {
      display: flex;
      flex-wrap: wrap;
    }

    .skill {
      width: 150px;
      margin: 10px;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
      text-align: center;
      cursor: pointer;
      transition: background-color 0.3s ease; 
    }

    .skill:hover {
      background-color: #f0f0f0; /* Highlight on hover */
    }

    .skill.active {
      background-color: #e0e0e0; /* More prominent highlight when active */
    }

    .skill-details {
      margin-top: 10px;
      display: none; /* Initially hidden */
    }
  </style>
</head>
<body>

  <h2>Skills</h2>

  <div class="skill-container">
    <div class="skill" data-details="details-1">
      <h3>Interior Design</h3>
    </div>
    <div class="skill" data-details="details-2">
      <h3>AutoCAD</h3>
    </div>
    <div class="skill" data-details="details-3">
      <h3>Attention to Detail</h3>
    </div>
    </div>

  <div id="details-1" class="skill-details">
    <p>Experienced in creating functional and aesthetically pleasing spaces for residential and commercial clients. Proficient in space planning, color theory, and material selection.</p>
  </div>

  <div id="details-2" class="skill-details">
    <p>Skilled in using AutoCAD software for 2D and 3D design and drafting.  Able to create accurate and detailed technical drawings for interior design projects.</p>
  </div>

  <div id="details-3" class="skill-details">
    <p>Highly detail-oriented with a proven ability to maintain accuracy and precision in design plans and project execution. </p>
  </div>

  <script>
    // JavaScript for interactivity
    const skills = document.querySelectorAll('.skill');
    skills.forEach(skill => {
      skill.addEventListener('click', () => {
        const detailsId = skill.getAttribute('data-details');
        const details = document.getElementById(detailsId);

        // Toggle active class for visual feedback
        skill.classList.toggle('active');

        // Show/hide the details
        if (details.style.display === "none") {
          details.style.display = "block";
        } else {
          details.style.display = "none";
        }
      });
    });
  </script>

</body>
</html>
