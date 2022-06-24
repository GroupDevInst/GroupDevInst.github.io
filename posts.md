---
layout: default
---

<style>
* {
    box-sizing: border-box;
}


/* The grid: Four equal columns that floats next to each other */
.column {
    float: left;
    width: 25%;
    padding: 10px;
}

/* Style the images inside the grid */
.column img {
    opacity: 0.8; 
    cursor: pointer; 
}

.column img:hover {
    opacity: 1;
}

/* Clear floats after the columns */
.row:after {
    content: "";
    display: table;
    clear: both;
}

/* The expanding image container */
.container {
    position: relative;
    display: none;
}

/* Expanding image text */
#imgtext {
    position: absolute;
    bottom: 15px;
    left: 15px;
    color: white;
    font-size: 20px;
}


</style>
</head>
<body>

<!-- The four columns -->
<div class="row">
  <div class="column">
    <img src="photo1_1.jpg" alt="" style="width:100%" onclick="myFunction(this);">
  </div>
  <div class="column">
    <img src="photo1_2.jpg" alt="" style="width:100%" onclick="myFunction(this);">
  </div>
  <div class="column">
    <img src="photo1_3.jpg" alt="" style="width:100%" onclick="myFunction(this);">
  </div>
  <div class="column">
    <img src="photo2_1.jpg" alt="" style="width:100%" onclick="myFunction(this);">
  </div>
  <div class="column">
    <img src="photo2_2.jpg" alt="" style="width:100%" onclick="myFunction(this);">
  </div>
  <div class="column">
    <img src="photo2_3.jpg" alt="" style="width:100%" onclick="myFunction(this);">
  </div>
</div>

<div class="container">
  <img id="expandedImg" style="width:100% ">
  <div id="imgtext"></div>
</div>

<script>
function myFunction(imgs) {
    var expandImg = document.getElementById("expandedImg");
    var imgText = document.getElementById("imgtext");
    expandImg.src = imgs.src;
    imgText.innerHTML = imgs.alt;
    expandImg.parentElement.style.display = "block";
}
</script>

</body>
</html>
