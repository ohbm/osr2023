---
layout: page
title: Open Science 101
---

<html>

<div class="input-group rounded">
    <input id="search-input" type="search" class="input-group-text form-control rounded" placeholder="Search" aria-label="Search" aria-describedby="search-addon" />
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
        educationalHTML += `
            <tr>
                <td>
                    <a href=${educational.Link}>${educational.Name}</a>
                </td>
            </tr>
        `;
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
