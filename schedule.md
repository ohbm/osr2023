---
layout: page
title: Schedule
---


<script>
const ALL_DAYS = ["07-23", "07-24", "07-25", "07-26"];

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
  <div id="day-07-23" class="schedule-day active" onclick="showScheduleForDay('07-23')">July 23</div>
  <div id="day-07-24" class="schedule-day" onclick="showScheduleForDay('07-24')">July 24</div>
  <div id="day-07-25" class="schedule-day" onclick="showScheduleForDay('07-25')">July 25</div>
  <div id="day-07-26" class="schedule-day" onclick="showScheduleForDay('07-26')">July 26</div>
</div>

<h5 style="text-align: center;">
GMT-4
</h5>

<div id="schedule-07-23" class="schedule-block">
    <h4>July 23, Sunday</h4>

    <div class="schedule-content">
        <table class="osr-schedule">
            <tr>
                <td>GMT-4</td>
                <td>OPEN SCIENCE ROOM</td>
            </tr>
            <tr>
                <td>8:00-9:00</td>
                <td>
                    <div>OSR Panel 1: Telehealth as a tool for open data research and sharing</div>
                    <div><a href="https://www.crowdcast.io/" target="_blank">Watch on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>10:30-11:30</td>
                <td>
                    <div>OSR: Emergent Session #1</div>
                    <div><a href="https://www.crowdcast.io/" target="_blank">Watch on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>11:30-12:15</td>
                <td>
                    <div>OSR Table Talk 1: Telehealth as a tool for open data research and sharing in neurosciences</div>
                    <div><a href="https://www.crowdcast.io/" target="_blank">Watch on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>14:15-15:30</td>
                <td>
                    <div>OSR Panel 2: Evolution of open publishing (To do or not to do?/Lessons learnt)</div>
                    <div><a href="https://www.crowdcast.io/" target="_blank">Watch on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>16:45-17:30</td>
                <td>
                    <div>OSR Table Talk 2: Evolution of open publishing (To do or not to do?/Lessons learnt)</div>
                    <div><a href="https://www.crowdcast.io/" target="_blank">Watch on Crowdcast</a></div>
<!--                     <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4a43a7c9374f60d948fd/" data-event="629a4a43a7c9374f60d948fd" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-style="1">Add to Calendar</a> -->
                </td>
            </tr>
        </table>
    </div>
</div>

<div id="schedule-07-24" class="schedule-block">
    <h4>July 24, Tuesday</h4>

    <div class="schedule-content">
        <table class="osr-schedule">
            <tr>
                <td>GMT-4</td>
                <td>OPEN SCIENCE ROOM</td>
            </tr>
            <tr>
                <td>8:00-9:00</td>
                <td>
                    <div>Panel 4: Emerging Statistical Perspectives in Promoting Reproducible Research</div>
                    <div><a href="https://www.crowdcast.io/e/panel-4-emerging-statistical" target="_blank">Replay on Crowdcast</a></div>
<!--                     <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4b4210e33846f6e40e62/" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a4b4210e33846f6e40e62" data-style="1">Add to Calendar</a> -->
                </td>
            </tr>
            <tr>
                <td>10:30-11:30</td>
                <td>
                    <div>Emergent #8: Discussion of priorities for multi-echo fMRI methods development</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-8" target="_blank">Replay on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>12:45-13:45</td>
                <td>
                    <div>Table Talk 2: Charting a career path after the PhD with Thomas Yeo</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--charting" target="_blank">Replay on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>14:45-15:45</td>
                <td>
                    <div>Emergent #9: NeuroLibre reproducible preprint server</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-9" target="_blank">Replay on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>17:00-18:00</td>
                <td>
                    <div>Emergent #10: Towards an Open Developer Community for Neuroimaging MATLAB Community Toolboxes</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-10" target="_blank">Replay on Crowdcast</a></div>
                </td>
            </tr>
        </table>
    </div>
</div>

<div id="schedule-07-25" class="schedule-block">
    <h4>July 25, Wednesday</h4>

    <div class="schedule-content">
        <table class="osr-schedule">
            <tr>
                <td>GMT-4</td>
                <td>OPEN SCIENCE ROOM</td>
            </tr>
            <tr>
                <td>8:00-9:00</td>
                <td>
                    <div>Panel 4: Emerging Statistical Perspectives in Promoting Reproducible Research</div>
                    <div><a href="https://www.crowdcast.io/e/panel-4-emerging-statistical" target="_blank">Replay on Crowdcast</a></div>
<!--                     <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4b4210e33846f6e40e62/" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a4b4210e33846f6e40e62" data-style="1">Add to Calendar</a> -->
                </td>
            </tr>
            <tr>
                <td>10:30-11:30</td>
                <td>
                    <div>Emergent #8: Discussion of priorities for multi-echo fMRI methods development</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-8" target="_blank">Replay on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>12:45-13:45</td>
                <td>
                    <div>Table Talk 2: Charting a career path after the PhD with Thomas Yeo</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--charting" target="_blank">Replay on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>14:45-15:45</td>
                <td>
                    <div>Emergent #9: NeuroLibre reproducible preprint server</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-9" target="_blank">Replay on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>17:00-18:00</td>
                <td>
                    <div>Emergent #10: Towards an Open Developer Community for Neuroimaging MATLAB Community Toolboxes</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--emergent-10" target="_blank">Replay on Crowdcast</a></div>
                </td>
            </tr>
        </table>
    </div>
</div>
<div id="schedule-07-26" class="schedule-block">

    <h4>July 26, Thursday</h4>

    <div class="schedule-content">   
        <table class="osr-schedule">
            <tr>
                <td>GMT-4</td>
                <td>OPEN SCIENCE ROOM</td>
            </tr>
            <tr>
                <td>8:00-9:00</td>
                <td>
                    <div>Reflection about OHBM (Combined SIGs Event)</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--reflections" target="_blank">Replay on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>10:30-11:30</td>
                <td>
                    <div>Panel 5: Social Bias in Machine Learning</div>
                    <div><a href="https://www.crowdcast.io/e/panel-5-social-bias" target="_blank">Replay on Crowdcast</a></div>
<!--                     <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4ba20de33e392ef7ff06/" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a4ba20de33e392ef7ff06" data-style="1">Add to Calendar</a> -->
                </td>
            </tr>
            <tr>
                <td>11:45-12:45</td>
                <td>
                    <div>Table Talk 3: Reproducible Science and my role in it with Thomas Nichols</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--reproducible" target="_blank">Replay on Crowdcast</a></div>
                </td>
            </tr>
            <tr>
                <td>12:45-13:00</td>
                <td>
                    <div>Closing Ceremony</div>
                    <div><a href="https://www.crowdcast.io/e/osr-2022--closing" target="_blank">Replay on Crowdcast</a></div>
                </td>
            </tr>
            
            
        </table>
    </div>
</div>

<div class="schedule-leave-space-before-footer">
<!--     <a href="https://calendar.google.com/calendar/u/0?cid=MjQydjZtZGFpcWQydWM0YzVlNDcxazA2Nm9AZ3JvdXAuY2FsZW5kYXIuZ29vZ2xlLmNvbQ" target="_blank">CLICK HERE to add the OSR schedule to your Google calendar!</a> -->
</div>

<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src='https://plugins.eventable.com/eventable.js';fjs.parentNode.insertBefore(js,fjs);}}(document,'script', 'eventable-script');</script>

