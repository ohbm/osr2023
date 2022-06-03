---
layout: page
title: Panel Themes in 2022
---

<html>
<script>

function getPanelSpeakersForPanelName(panelName) {
  const speakers = {{ site.data.speakers | jsonify }};
  const panelSpeakers = speakers.filter(speaker => speaker.Panel !== undefined);
  return panelSpeakers.filter(speaker => (speaker.Panel.toLowerCase().includes(panelName.toLowerCase())));
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
  const out = element ? element : "";
  return out;
}

function formatSpeakerDiv(speaker) {
  console.log(speaker.Website);

  const speakerUrl = getUrlForSpeaker(speaker);

  return `
    <a style="display:block; color:#05323F" href="${speakerUrl}">
      <img src="../img/speakers/${speaker.Name.toLowerCase().replaceAll(' ', '_')}.jpg" style="height:200px; border-radius:50%;">
      
      <h3>${speaker.Name}</h3>
      <h4>${emptyStringForNull(speaker.Job)}</h4>

      <h6>${emptyStringForNull(speaker.Affiliation)}</h6>
    </a>
  `;
}

function displayPanel(panelName) {
  const speakers = getPanelSpeakersForPanelName(panelName);
  return `
    ${speakers.map(formatSpeakerDiv).join("")}
  `;
}

</script>
</html>


The OSR has always been a place to learn and share experiences.
This year we are centering these experiences around themes which are undergoing rapid change in our discipline.

## Theme 1: Challenges of Open Science in Developing Countries
When: 8:00 GMT+1 | June 20, 2022 (Monday) <br/>
<br/>
This panel is aimed at discussing the challenges that are faced by these countries, which are related to the availability of educational technology, including access to adequate online learning resources, opportunities for data processing training and professional development. We will discuss the coordinated actions that can be taken in order to support and implement open science-based research in an environment that has limited economic resources.  <br/>
Points to be discussed or general misconceptions to be demystified include: 
* My technical training has been limited: How can I contribute to open science? 
* My data is not worth sharing: Should I make my data open? 
* I do not have enough funding: Do I have enough resources to practice open publishing? 
* My network is too limited: How can I connect with the community to share code and contribute to projects?  
* I don’t have enough computing resources to work with open datasets like the Human Connectome Project. What can I do? 

<html>
<div class="panel-speakers" id="open-science-panel"></div>

<script>
document.getElementById("open-science-panel").innerHTML = displayPanel("Open Science");
</script>
</html>

## Theme 2: Open Publishing
When: 14:45 GMT+1 | June 20, 2022 (Monday) <br/>
<br/>
How will publishing high-quality research contributions including negative results and sharing supporting code and data, with an emphasis on replicability add value and move science forward? What are long term objectives and feasible actions for everyday researchers including established PIs, early career researchers (ECRs), as well as PhD students. <br/>
<br/>
Topics and questions for discussion will include: 
* Publication bias 
* Will a standard publication still largely exist of a non-interactive written document in 10 year's time, or do you think the essence of publishing will change? 
* There has been a lot of criticism of the peer review system. What are your thoughts about the future of peer review? 
* The tension between for-profit publishers and academic values has been the topic of many Twitter debates and reviewing boycotts. How do your journals balance cost and benefit? 
* What can authors and reviewers do now to improve open science practices in publishing? 

<html>
<div class="panel-speakers" id="open-publishing-panel"></div>

<script>
document.getElementById("open-publishing-panel").innerHTML = displayPanel("Open Publishing");
</script>
</html>


## Theme 3: Open Code: Myths Debunked
When: 14:45 GMT+1 | June 21, 2022 (Tuesday) <br/>
<br/>
Are you unsure of whether to share your code because of time constraint, getting scooped, or other common fears? Or is your ‘lab culture’ not keen on sharing code? This panel will discuss and debunk common myths for new coders and newbies to open science who are unsure of or not allowed to share their code. Not only will the speakers provide an open platform to discuss the benefits of open code but will expose common myths and share helpful resources on how to write good code, maintain, and share it.  <br/>
<br/>
Myths to be debunked: 
* I can only share my code if it is a complete software package  
* I can only share my code if I am committed to providing ongoing support. 
* I can only share my code if I am a trained software engineer. 
* Sharing my code is not worth the time and effort. 
* If I share my code, I’m going to get scooped/criticized. 
* I am in a lab where sharing code is not a common practice, so I can’t share the code from my projects. 

<html>
<div class="panel-speakers" id="open-code-panel"></div>

<script>
document.getElementById("open-code-panel").innerHTML = displayPanel("Open Code");
</script>
</html>


## Theme 4: Emerging Statistical Perspectives in Promoting Reproducible Research 
When: 8:00 GMT+1 | June 22, 2022 (Wednesday) <br/>
<br/>
Important questions have been raised regarding how typical study designs and methods can impair both sensitivity and specificity —and, as a result, reproducibility. This panel will discuss emerging ideas about how we can mitigate these issues by rethinking statistical methods and data collection. Reflecting on this discussion, we will examine how we should prioritize these solutions. This will be less of a didactic session about widely accepted best practices and more of a collaborative discussion about open questions for further innovation.<br/>
<br/>
Possible questions include: 
* Inference 
  + What sorts of data should we prioritize (e.g., big, deep, multimodal, etc.)? 
  + Do small effect sizes imply that results are meaningless? 
  + Crises, variability and reproducibility: alarmism versus realism 
  + Alternative perspectives of univariate mass modeling and multiple comparisons? 
  + Challenges in studying individual differences? 
* Pipelines and physiological signal 
  + Should we mitigate or embrace pipeline multiplicity? 
  + In what ways can we think of physiological influences as confound versus information? 


<html>
<div class="panel-speakers" id="statistical-perspectives-panel"></div>

<script>
document.getElementById("statistical-perspectives-panel").innerHTML = displayPanel("Statistical Perspectives");
</script>
</html>

## Theme #5: Social Bias in Machine Learning  
When: 10:30 GMT+1 | June 23, 2022 (Thursday) <br/>
<br/>
Prediction algorithms are increasingly common in neuroimaging research and offer many opportunities for clinical care and personalized medicine. However, inadvertent outcomes can lead to predictions that are influenced by race, gender, sexuality, and ethnicity, or privileging one arbitrary group of users over others. Social bias can be introduced due to factors such as small dataset, sampling bias, and researcher introduced error among many others. This panel is aimed at discussing the relevant factors and possible feasible solutions on ways to conceptualize, measure, and mitigate social bias in machine learning.<br/>
<br/>
Specific questions and topics for discussion will include: 
* How can you measure the fairness or social bias of a prediction algorithm? 
* What would a dataset without social bias look like? 
* In addition to social biases that have come to light (related to e.g., gender, race, ethnicity etc.), there may be other biases that have not yet been considered. As such, is an unbiased algorithm ever fully achievable? 


<html>
<div class="panel-speakers" id="social-bias-panel"></div>

<script>
document.getElementById("social-bias-panel").innerHTML = displayPanel("Social Bias");
</script>
</html>
