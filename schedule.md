---
layout: page
title: Schedule
---


<script>
const ALL_DAYS = ["06-20", "06-21", "06-22", "06-23"];

function setupActiveDayTab(activeDay) {
    /* First, remove the "active" classname for all tabs */
    ALL_DAYS.forEach(day => {
        let divDay = document.getElementById(`day-${day}`);
        divDay.className = divDay.className.replace("active", "");
    });
    
    /* Then add it to the appropriate day */
    let divDay = document.getElementById(`day-${activeDay}`);
    divDay.className = `${divDay.className} active`;
}

function setupActiveDaySchedule(activeDay) {
    /* First, hide all the schedule blocks */
    ALL_DAYS.forEach(day => {
        let divDay = document.getElementById(`schedule-${day}`);
        divDay.className = divDay.className.replace("active", "");
    });
    
    /* Then display:block to show the appropriate one */
    let divDay = document.getElementById(`schedule-${activeDay}`);
    divDay.className = `${divDay.className} active`;
}

function showScheduleForDay(day) {
    setupActiveDayTab(day);
    setupActiveDaySchedule(day);
}
</script>


<div class="schedule-days">
  <div id="day-06-20" class="schedule-day active" onclick="showScheduleForDay('06-20')">June 20</div>
  <div id="day-06-21" class="schedule-day" onclick="showScheduleForDay('06-21')">June 21</div>
  <div id="day-06-22" class="schedule-day" onclick="showScheduleForDay('06-22')">June 22</div>
  <div id="day-06-23" class="schedule-day" onclick="showScheduleForDay('06-23')">June 23</div>
</div>

<h5 style="text-align: center;">
GMT+1
</h5>


<div id="schedule-06-20" class="schedule-block active">
    <h4>June 20, Monday</h4>

    <div class="schedule-content">
        <table class="osr-schedule">
            <tr>
                <td>GMT+1</td>
                <td>OPEN SCIENCE ROOM</td>
            </tr>
            <tr>
                <td>8:00-8:15</td>
                <td>
                    <div>Opening Ceremony with ☕</div>
                    <div><a href="https://www.crowdcast.io/e/panel-1-challenges-of" target="_blank">Click here to join this session!</a></div>
                </td>

            </tr>
            <tr>
                <td>8:15-9:15</td>
                <td>
                    <div>Panel 1: Challenges of Open Science in Developing Countries</div>
                    <div><a href="https://www.crowdcast.io/e/panel-1-challenges-of" target="_blank">Click here to join this panel!</a></div>
                    <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a28568622ac08962b8c7f" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a28568622ac08962b8c7f" data-style="1">Add to Calendar</a>
                </td>
            </tr>
            <tr>
                <td>10:30-12:15</td>
                <td>
                    <div>Emergent #1: BIDS Town Hall</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
            <tr>
                <td>14:45-15:45</td>
                <td>
                    <div>Panel 2: Open Publishing</div>
                    <div><a href="https://www.crowdcast.io/e/panel-2-open-publishing" target="_blank">Click here to join this panel!</a></div>
                    <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4a43a7c9374f60d948fd/" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a4a43a7c9374f60d948fd" data-style="1">Add to Calendar</a>
                </td>
            </tr>
            <tr>
                <td>16:45-17:45</td>
                <td>
                    <div>Emergent #2: COINSTAC: A futuristic framework for collaborative big-data research</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-2" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
            <tr>
                <td>18:00-19:00</td>
                <td>
                    <div>Emergent #3: Harmonized analysis of fMRI data using HALFpipe</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-3" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
        </table>
    </div>
</div>

<div id="schedule-06-21" class="schedule-block">
    <h4>June 21, Tuesday</h4>

    <div class="schedule-content">
        <table class="osr-schedule">
            <tr>
                <td>GMT+1</td>
                <td>OPEN SCIENCE ROOM</td>
            </tr>
            <tr>
                <td>8:00-9:00</td>
                <td>
                    <div>Emergent #4: Brainstorming features and ideas for AFNI</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-4" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
            <tr>
                <td>10:15-11:15</td>
                <td>
                    <div>Emergent #5: Snakebids: Reproducible neuroimaging workflows as BIDS apps</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-5" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
            <tr>
                <td>11:15-12:15</td>
                <td>
                    <div>Emergent #6: How the Neuroimaging Tools & Resources Collaboratory (NITRC) can help your research</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-6" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
            <tr>
                <td>12:15-13:00</td>
                <td>
                    <div>Table Talk 1: Open Publishing with Tonya White</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--open-pub" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
            <tr>
                <td>14:45-15:45</td>
                <td>
                    <div>Panel 3: Open Code - 6 Myths Debunked</div>
                    <div><a href="https://www.crowdcast.io/e/panel-3-open-code-6" target="_blank">Click here to join this panel!</a></div>
                    <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4a43a7c9374f60d948fd/" data-event="629a4a43a7c9374f60d948fd" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-style="1">Add to Calendar</a>
                </td>
            </tr>
            <tr>
                <td>17:45-18:45</td>
                <td>
                    <div>Emergent #7: Physiopy open meeting: Best practices in using physiological data to denoise functional timeseries</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-7" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
        </table>
    </div>
</div>

<div id="schedule-06-22" class="schedule-block">
    <h4>June 22, Wednesday</h4>

    <div class="schedule-content">
        <table class="osr-schedule">
            <tr>
                <td>GMT+1</td>
                <td>OPEN SCIENCE ROOM</td>
            </tr>
            <tr>
                <td>8:00-9:00</td>
                <td>
                    <div>Panel 4: Emerging Statistical Perspectives in Promoting Reproducible Research</div>
                    <div><a href="https://www.crowdcast.io/e/panel-4-emerging-statistical" target="_blank">Click here to join this panel!</a></div>
                    <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4b4210e33846f6e40e62/" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a4b4210e33846f6e40e62" data-style="1">Add to Calendar</a>
                </td>
            </tr>
            <tr>
                <td>10:30-11:30</td>
                <td>
                    <div>Emergent #8: Discussion of priorities for multi-echo fMRI methods development</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-8" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
            <tr>
                <td>12:45-13:45</td>
                <td>
                    <div>Table Talk 2: Charting a career path after the PhD with Thomas Yeo</div>
<!--                     <div><a href="https://www.crowdcast.io/e/osr-2022--charting" target="_blank">Click here to join this session!</a></div> -->
                </td>
            </tr>
            <tr>
                <td>14:45-15:45</td>
                <td>
                    <div>Emergent #9: NeuroLibre reproducible preprint server</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-9" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
            <tr>
                <td>17:00-18:00</td>
                <td>
                    <div>Emergent #10: Towards an Open Developer Community for Neuroimaging MATLAB Community Toolboxes</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-10" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
        </table>
    </div>
</div>
<div id="schedule-06-23" class="schedule-block">

    <h4>June 23, Thursday</h4>

    <div class="schedule-content">   
        <table class="osr-schedule">
            <tr>
                <td>GMT+1</td>
                <td>OPEN SCIENCE ROOM</td>
            </tr>
            <tr>
                <td>8:00-9:00</td>
                <td>
                    <div>Reflection about OHBM (Combined SIGs Event)</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--reflections" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
            <tr>
                <td>10:30-11:30</td>
                <td>
                    <div>Panel 5: Social Bias in Machine Learning</div>
                    <div><a href="https://www.crowdcast.io/e/panel-5-social-bias" target="_blank">Click here to join this panel!</a></div>
                    <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4ba20de33e392ef7ff06/" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a4ba20de33e392ef7ff06" data-style="1">Add to Calendar</a>
                </td>
            </tr>
            <tr>
                <td>11:45-12:45</td>
                <td>
                    <div>Table Talk 3: Reproducible Science and my role in it with Thomas Nichols</div>
<!--                     <div><a href="https://www.crowdcast.io/e/osr-2022--reproducible" target="_blank">Click here to join this session!</a></div> -->
                </td>
            </tr>
            <tr>
                <td>12:45-13:00</td>
                <td>
                    <div>Closing Ceremony</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--closing" target="_blank">Click here to join this session!</a></div>
                </td>
            </tr>
        </table>
    </div>

</div>

<div class="schedule-leave-space-before-footer">
    <a href="https://calendar.google.com/calendar/u/0?cid=MjQydjZtZGFpcWQydWM0YzVlNDcxazA2Nm9AZ3JvdXAuY2FsZW5kYXIuZ29vZ2xlLmNvbQ" target="_blank">CLICK HERE to add the OSR schedule to your Google calendar!</a>
</div>

<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src='https://plugins.eventable.com/eventable.js';fjs.parentNode.insertBefore(js,fjs);}}(document,'script', 'eventable-script');</script>

