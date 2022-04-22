---
layout: page
title: Open Science 101
---

<html>

<div>
    <input
        id="search-input"
        type="search"
        class="input-group-text form-control rounded"
        placeholder="Search"
        aria-label="Search"
        aria-describedby="search-addon"
    />
</div>

<!-- This divs are rendered dynamically by the javascript functions below based on the _data/educationals.csv file -->
<div id="tags-contents" class="educational-tags-container"></div>
<div id="educational-contents"></div>



<script>
function getUniqueTags() {
    const educationals = {{ site.data.educational | jsonify }};
    let allTags = [].concat.apply([], educationals.map(educ => educ.Tags.split(',')));
    allTags.push("All");
    const uniqueTags = [...new Set(allTags)];
    uniqueTags.sort();

    return uniqueTags
}

function getTagColorClassName(tag) {
    const availableColors = ["", "orange-tag", "green-tag"];
    const allTags = getUniqueTags();

    const tagPosition = allTags.indexOf(tag);
    
    return availableColors[tagPosition % availableColors.length];
}

function getFilteredEducationalsByContent(filterValue) {
    const educationals = {{ site.data.educational | jsonify }};
    return educationals.filter(educ => (educ.Name.toLowerCase().includes(filterValue.toLowerCase())));
}
function getFilteredEducationalsByTag(tagValue) {
    const educationals = {{ site.data.educational | jsonify }};
    return educationals.filter(educ => (educ.Tags.toLowerCase().includes(tagValue.toLowerCase())));
}

function renderEducationalDiv(educationals) {
    let educationalHTML = "<div class='educational-cards'>";

    <!-- Create a card for each educational content which contains a clickable title, a description if available and the tags -->
    educationals.map((educational) => {
        const titleDiv = `<div class='educational-card-title'><a href=${educational.Link}>${educational.Name}</a></div>`;
        // const tagsDiv = `<div class='educational-card-tags'><div class="btn btn-primary tag-button">NiPreps</div></div>`;
        let tagsDiv = `<div class='educational-card-tags'>`;
        educational.Tags.split(",").map(tag => {
            const tagColorClassName = getTagColorClassName(tag);
            tagsDiv += `<div class="btn btn-primary tag-button ${tagColorClassName}">${tag}</div>`;
        });
        tagsDiv += `</div>`;
        const descriptionDiv = `<div class='educational-card-description'>${educational.Description}</div>`;
        educationalHTML += `
            <div class='educational-card'>
                ${titleDiv}
                ${descriptionDiv}
                ${tagsDiv}
            </div>
        `;
    });
    educationalHTML += "</div>";

    // Finally add the cards inside the appropriate div
    document.getElementById("educational-contents").innerHTML = educationalHTML;
}

function renderAllEducationals() {
    renderEducationalDiv({{ site.data.educational || jsonify }});
}

function renderTags() {
    let tags = getUniqueTags();

    // Add additional "All" tag to let user reset the list
    let tagsHTML= ""
    // let tagsHTML = "<a class='btn btn-primary tag-button ${getTagColorClassName('All')}'>All</a>";
    // Add all other tags available in the educationals data file
    tags.map((tag) => {
        const tagColorClassName = getTagColorClassName(tag);
        tagsHTML += `<a class="btn btn-primary tag-button ${tagColorClassName}">${tag}</a>`;
    });

    document.getElementById("tags-contents").innerHTML = tagsHTML;
}

renderTags();
renderAllEducationals();

<!-- Add listeners to handle interactions with the search -->

<!-- This first one is the filtering by clicking on the tag buttons -->
let tagButtons = document.getElementsByClassName("tag-button");
for (let index = 0; index < tagButtons.length; index++) {
    tagButtons[index].addEventListener('click', (event) => {
        <!-- If the value is "All", it means we want to display all the cards -->
        const tagValue = event.target.outerText === "All" ? "" : event.target.outerText;
        const filteredEducationals = getFilteredEducationalsByTag(tagValue);
        renderEducationalDiv(filteredEducationals);
    })
}

<!-- This second one is by leveraging what the users write in the search bar -->
document.getElementById('search-input').addEventListener('keyup', (event) => {
    const inputValue = event.target.value;
    const filteredEducational = getFilteredEducationalsByContent(inputValue);
    renderEducationalDiv(filteredEducational);
});

</script>



</html>
