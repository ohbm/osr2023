---
layout: page
title: Speakers
---


We are excited to host a wonderful list of speakers in the Open Science Room.
They will be contributing Educational sessions and panel discussions.
Click on a speaker below to see their bio and talk details.

Emergent sessions are spontaneous in nature, so speaker will not appear in advanced in this page!

<br>

<html>

<div class="input-group rounded">
  <input id="search-input" type="search" class="form-control rounded" placeholder="Search" aria-label="Search" aria-describedby="search-addon" />
  <span class="input-group-text border-0" id="search-addon">
    <i class="fas fa-search"></i>
  </span>
</div>

<div id="educational-contents"></div>



<script>
function getFilteredEducationalContent(filterValue) {
    const educationals = {{ site.data.educational | jsonify }};
    return educationals.filter(educ => (educ.Name.toLowerCase().includes(filterValue.toLowerCase())));
}

function renderEducationalDiv(educationals) {
    let educationalHTML = "<table>";
    educationals.map((educational) => {
        educationalHTML += `<tr><td><a href=${educational.Link}>${educational.Name}</a></td></tr>`
    });
    educationalHTML += "</table>";

    document.getElementById("educational-contents").innerHTML = educationalHTML;
}

function initialRender() {
    renderEducationalDiv({{ site.data.educational || jsonify }});
}

initialRender();

document.getElementById('search-input').addEventListener('keyup', (event) => {
    const inputValue = event.target.value;
    const filteredEducational = getFilteredEducationalContent(inputValue);
    renderEducationalDiv(filteredEducational);
});
</script>



</html>

