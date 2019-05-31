---
Header: "Video Exhibit"
layout: page
title: Video Exhibit
description: Walk Through Palestine.
background: '/img/lim.jpg'
---

<style>
.filterDiv {
  float: left;
  <!--background-color: #2196F3;
  color: #ffffff;-->
  width: 300px;
  line-height: 50px;
  text-align: center;
  margin: 5px;
  display: none;
}

.show {
  display: block;
}

.container {
  margin-top: 20px;
  overflow: hidden;
}

<!--* Style the buttons-->
.btn {
  border: none;
  outline: none;
  padding: 12px 16px;
  background-color: #f1f1f1;
  cursor: pointer;
}

.btn:hover {
  background-color: #ddd;
}

.btn.active {
  background-color: #666;
  color: white;
}
</style>
<body>

<h2>Go for a "Walk" in the Gaza Strip</h2>
<br>

<div id="myBtnContainer">
  <button class="btn active" onclick="filterSelection('all')"> Show all</button>
  <button class="btn" onclick="filterSelection('water')"> Water</button>
  <button class="btn" onclick="filterSelection('municipality')"> Municipality</button>
  <button class="btn" onclick="filterSelection('urban')"> Urban</button>
  <button class="btn" onclick="filterSelection('street-art')"> Street Art</button>
  <button class="btn" onclick="filterSelection('half-body')"> Partial Bodies</button>
  <button class="btn" onclick="filterSelection('construction')"> Construction</button>
  <button class="btn" onclick="filterSelection('tech')"> Tech</button>
  <button class="btn" onclick="filterSelection('store')"> Store</button>
</div>

<div class="container">
  <div class="filterDiv water"><iframe width="350px" height="250px" src="https://www.youtube.com/embed/s1WJsipsZkY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
  <div class="filterDiv water"><iframe width="350px" height="250px" src="https://www.youtube.com/embed/MNzdgkAwuIc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
  <div class="filterDiv water"><iframe width="350px" height="250px" src="https://www.youtube.com/embed/tGXtAAY6ehg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
  <div class="filterDiv municipality urban"><iframe width="350px" height="250px" src="https://www.youtube.com/embed/fsVLCHEQb74" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
  <div class="filterDiv urban street-art"><iframe width="350px" height="250px" src="https://www.youtube.com/embed/C1j_YHMMG4w" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
  <div class="filterDiv half-body"><iframe width="350px" height="250px" src="https://www.youtube.com/embed/fSBDY5vOkes" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
  <div class="filterDiv construction"><iframe width="350px" height="250px" src="https://www.youtube.com/embed/bK1ZuJS3SbU?rel=0&amp;showinfo=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
  <div class="filterDiv urban tech store"><iframe width="350px" height="250px" src="https://www.youtube.com/embed/hfkbvv_Nz2o" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
  <div class="filterDiv fruits">Melon</div>
  <div class="filterDiv fruits animals">Kiwi</div>
  <div class="filterDiv fruits">Banana</div>
  <div class="filterDiv fruits">Lemon</div>
  <div class="filterDiv animals">Cow</div>
</div>

<script>
filterSelection("all")
function filterSelection(c) {
  var x, i;
  x = document.getElementsByClassName("filterDiv");
  if (c == "all") c = "";
  for (i = 0; i < x.length; i++) {
    w3RemoveClass(x[i], "show");
    if (x[i].className.indexOf(c) > -1) w3AddClass(x[i], "show");
  }
}

function w3AddClass(element, name) {
  var i, arr1, arr2;
  arr1 = element.className.split(" ");
  arr2 = name.split(" ");
  for (i = 0; i < arr2.length; i++) {
    if (arr1.indexOf(arr2[i]) == -1) {element.className += " " + arr2[i];}
  }
}

function w3RemoveClass(element, name) {
  var i, arr1, arr2;
  arr1 = element.className.split(" ");
  arr2 = name.split(" ");
  for (i = 0; i < arr2.length; i++) {
    while (arr1.indexOf(arr2[i]) > -1) {
      arr1.splice(arr1.indexOf(arr2[i]), 1);     
    }
  }
  element.className = arr1.join(" ");
}

// Add active class to the current button (highlight it)
var btnContainer = document.getElementById("myBtnContainer");
var btns = btnContainer.getElementsByClassName("btn");
for (var i = 0; i < btns.length; i++) {
  btns[i].addEventListener("click", function(){
    var current = document.getElementsByClassName("active");
    current[0].className = current[0].className.replace(" active", "");
    this.className += " active";
  });
}
</script>

</body>
