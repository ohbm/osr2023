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
                <td>Open Science Room</td>
            </tr>
            <tr>
                <td>8:00 ➡ 8:15</td>
                <td>Opening Ceremony with ☕</td>
            </tr>
            <tr>
                <td>8:15 ➡ 9:15</td>
                <td>
                    <div>Panel 1: Challenges of Open Science in Developing Countries</div>
                    <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a28568622ac08962b8c7f" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a28568622ac08962b8c7f" data-style="1">Add to Calendar</a>
                </td>
            </tr>
            <tr>
                <td>10:30 ➡ 12:15</td>
                <td>Emergent #1: BIDS Town Hall</td>
            </tr>
            <tr>
                <td>14:45 ➡ 15:45</td>
                <td>
                    <div>Panel 2: Open Publishing</div>
                    <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4a43a7c9374f60d948fd/" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a4a43a7c9374f60d948fd" data-style="1">Add to Calendar</a>
                </td>
            </tr>
            <tr>
                <td>16:45 ➡ 17:45</td>
                <td>
                    </div>Emergent #2</div>
                    <a href="https://ohbm.github.io/osr2022/submit/" target="_blank">Request an Emergent Session</a>
                </td>
            </tr>
            <tr>
                <td>18:00 ➡ 19:00</td>
                <td>
                    </div>Emergent #3</div>
                    <a href="https://ohbm.github.io/osr2022/submit/" target="_blank">Request an Emergent Session</a>
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
                <td>Open Science Room</td>
            </tr>
            <tr>
                <td>8:00 ➡ 9:00</td>
                <td>
                    </div>Emergent #4</div>
                    <a href="https://ohbm.github.io/osr2022/submit/" target="_blank">Request an Emergent Session</a>
                </td>
            </tr>
            <tr>
                <td>10:15 ➡ 11:15</td>
                <td>
                    </div>Emergent #5</div>
                    <a href="https://ohbm.github.io/osr2022/submit/" target="_blank">Request an Emergent Session</a>
                </td>
            </tr>
            <tr>
                <td>11:15 ➡ 12:15</td>
                <td>
                    </div>Emergent #6</div>
                    <a href="https://ohbm.github.io/osr2022/submit/" target="_blank">Request an Emergent Session</a>
                </td>
            </tr>
            <tr>
                <td>12:15 ➡ 13:00</td>
                <td>Table Talk 1: Open Publishing with Tonya White</td>
            </tr>
            <tr>
                <td>14:45 ➡ 15:45</td>
                <td>
                    <div>Panel 3: Open Code - 6 Myths Debunked</div>
                    <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4abd1fd9d50830ca3664/" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-key="629a28543ef85c3ac00e5e83" data-style="1">Add to Calendar</a>
                </td>
            </tr>
            <tr>
                <td>17:45 ➡ 18:45</td>
                <td>
                    </div>Emergent #7</div>
                    <a href="https://ohbm.github.io/osr2022/submit/" target="_blank">Request an Emergent Session</a>
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
                <td>Open Science Room</td>
            </tr>
            <tr>
                <td>8:00 ➡ 9:00</td>
                <td>
                    <div>Panel 4: Emerging Statistical Perspectives in Promoting Reproducible Research</div>
                    <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4b4210e33846f6e40e62/" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a4b4210e33846f6e40e62" data-style="1">Add to Calendar</a>
                </td>
            </tr>
            <tr>
                <td>10:30 ➡ 11:30</td>
                <td>
                    </div>Emergent #8</div>
                    <a href="https://ohbm.github.io/osr2022/submit/" target="_blank">Request an Emergent Session</a>
                </td>
            </tr>
            <tr>
                <td>11:45 ➡ 12:45</td>
                <td>Table Talk 2: Charting a career path after the PhD with Thomas Yeo</td>
            </tr>
            <tr>
                <td>14:45 ➡ 15:45</td>
                <td>
                    </div>Emergent #9</div>
                    <a href="https://ohbm.github.io/osr2022/submit/" target="_blank">Request an Emergent Session</a>
                </td>
            </tr>
            <tr>
                <td>17:00 ➡ 18:00</td>
                <td>
                    </div>Emergent #10</div>
                    <a href="https://ohbm.github.io/osr2022/submit/" target="_blank">Request an Emergent Session</a>
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
                <td>Open Science Room</td>
            </tr>
            <tr>
                <td>8:00 ➡ 9:00</td>
                <td>Reflection about OHBM (Combined SIGs Event)</td>
            </tr>
            <tr>
                <td>10:30 ➡ 11:30</td>
                <td>
                    <div>Panel 5: Social Bias in Machine Learning</div>
                    <a href="https://add.eventable.com/events/629a28543ef85c3ac00e5e83/629a4ba20de33e392ef7ff06/" class="eventable-link" target="_blank" data-key="629a28543ef85c3ac00e5e83" data-event="629a4ba20de33e392ef7ff06" data-style="1">Add to Calendar</a>
                </td>
            </tr>
            <tr>
                <td>11:45 ➡ 12:45</td>
                <td>Table Talk 3: Reproducible Science and my role in it with Thomas Nichols</td>
            </tr>
            <tr>
                <td>12:45 ➡ 13:00</td>
                <td>Closing Ceremony</td>
            </tr>
        </table>
    </div>

</div>

<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src='https://plugins.eventable.com/eventable.js';fjs.parentNode.insertBefore(js,fjs);}}(document,'script', 'eventable-script');</script>
