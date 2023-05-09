---
layout: page
title: Panels
---

<html>
<script>

function getPanelSpeakersForPanelName(panelName) {
  // Filter all speakers to select only those that are in the given panel
  const speakers = {{ site.data.speakers | jsonify }};
  const panelSpeakers = speakers.filter(speaker => speaker.Panel !== undefined);
  return panelSpeakers.filter(speaker => (speaker.Panel && speaker.Panel.toLowerCase().includes(panelName.toLowerCase())));
}

function getUrlForSpeaker(speaker) {
  // Take website if available, then twitter, then github
  if (speaker.Website) {
    return speaker.Website;
  }
  if (speaker.Twitter) {
    return speaker.Twitter;
  }
  if (speaker.Github) {
    return speaker.Github;
  }

  return "";
}

function emptyStringForNull(element) {
  // Return empty string if the element is null to prevent the display of "null" on the page
  const out = element ? element : "";
  return out;
}

function getImageAssetPathForSpeaker(speaker) {
  // Retrieve image path of the speaker photo
  return `../img/speakers/${speaker.Name.toLowerCase().replaceAll(' ', '_')}.jpg`;
}

function formatSpeakerDiv(speaker) {
  // Generate a card for speaker with photo | name | panel job | affiliation | twitter | github
  // Only the speaker name is mandatory but you should check that there is a SURNAME_NAME.jpg
  // photo in the img/speakers folder
  // For the other fields, it only appears if the value is defined in the _data/speakers.csv
  if (!speaker.Name || speaker.Name === "") {
    return "";
  }

  const speakerUrl = getUrlForSpeaker(speaker);

  return `
    <div>
      <a style="color:#05323F" href="${speakerUrl}">
        <img src=${getImageAssetPathForSpeaker(speaker)} />

        <h3>${speaker.Name}</h3>
        ${speaker.Job ? `<h4>${speaker.Job}</h4>` : ""}
        ${speaker.Affiliation ? `<h6>${speaker.Affiliation}</h6>` : ""}
      </a>
      ${speaker.Twitter ? `<a target="_blank" href="${speaker.Twitter}"><i class="fa fa-twitter fa-2x"></i></a>` : ""}
      ${speaker.GitHub ? `<a target="_blank" href="${speaker.GitHub}"><i class="fa fa-github fa-2x"></i></a>` : ""}
    </div>
  `;
}

function displayPanel(panelName) {
  // Generate divs that contain all the speakers that are in the given panel
  const speakers = getPanelSpeakersForPanelName(panelName);
  return `${speakers.map(formatSpeakerDiv).join("")}`;
}

</script>
</html>


The OSR has always been a place to learn and share experiences.
This year we are centering these experiences around themes which are undergoing rapid change in our discipline.

## Topic 1: Telehealth as a tool for open data research and sharing
### <a href="https://www.crowdcast.io" target="_blank">Watch on Crowdcast</a>
When: X:00 GMT-4 | July X, 2023 (X) <br/>
<!-- <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a28568622ac08962b8c7f" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a28568622ac08962b8c7f" data-style="1">Add to Calendar</a><br/> -->
<br/>

Text here !!!

<html>
<div class="panel-speakers" id="open-science-panel"></div>

<script>
document.getElementById("open-science-panel").innerHTML = displayPanel("Open Science");
</script>
</html>

## Topic 2: Evolution of open publishing (To do or not to do?/Lessons learnt)
### <a href="https://www.crowdcast.io" target="_blank">Watch on Crowdcast</a>
When: 14:45 GMT+1 | June 20, 2022 (Monday) <br/>
<!-- <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4a43a7c9374f60d948fd/" data-event="629a4a43a7c9374f60d948fd" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-style="1">Add to Calendar</a><br/> -->
<br/>
How will publishing high-quality research contributions including negative results and sharing supporting code and data, with an emphasis on replicability add value and move science forward? What are long term objectives and feasible actions for everyday researchers including established PIs, early career researchers (ECRs), as well as PhD students. <br/>
<br/>
 text here !!!
<html>
<div class="panel-speakers" id="open-publishing-panel"></div>

<script>
document.getElementById("open-publishing-panel").innerHTML = displayPanel("Open Publishing");
</script>
</html>


## Topic 3: Standardization of code
### <a href="https://www.crowdcast.io" target="_blank">Replay on Crowdcast</a>
When: 14:45 GMT+1 | June 21, 2022 (Tuesday) <br/>
<!-- <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4abd1fd9d50830ca3664/" data-event="629a4abd1fd9d50830ca3664" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-style="1">Add to Calendar</a><br/> -->
<br/>
text here !!! 
<html>
<div class="panel-speakers" id="open-code-panel"></div>

<script>
document.getElementById("open-code-panel").innerHTML = displayPanel("Open Code");
</script>
</html>


## Topic 4: Shareable resources in neuroimaging
### <a href="https://www.crowdcast.io" target="_blank">Watch on Crowdcast</a> 
When: 8:00 GMT+1 | June 22, 2022 (Wednesday) <br/>
<!-- <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4b4210e33846f6e40e62/" data-event="629a4b4210e33846f6e40e62" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-style="1">Add to Calendar</a><br/> -->
<br/>
text here!!! 
<html>
<div class="panel-speakers" id="statistical-perspectives-panel"></div>

<script>
document.getElementById("statistical-perspectives-panel").innerHTML = displayPanel("Statistical Perspectives");
</script>
</html>

## Topic 5: Large open data repositories: sustainability and global implications of reuse
### <a href="https://www.crowdcast.io" target="_blank">Watch on Crowdcast</a>  
When: 10:30 GMT+1 | June 23, 2022 (Thursday) <br/>
<!-- <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4ba20de33e392ef7ff06/" data-event="629a4ba20de33e392ef7ff06" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-style="1">Add to Calendar</a><br/> -->
<br/>
Text here!!!

<html>
<div class="panel-speakers" id="social-bias-panel"></div>

<script>
document.getElementById("social-bias-panel").innerHTML = displayPanel("Social Bias");
</script>
</html>
