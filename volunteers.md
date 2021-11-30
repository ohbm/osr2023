---
layout: page
title: Volunteers
---

The core OSR team were elected as part of the [OHBM Open Science Special Interest Group](https://ossig.netlify.app/#OSSIG_team) (OS-SIG).


<br>


<table class="people">
    <tr class="people">
        <td class="people">
            <a style="display:block; color:#05323F" href="../team_eva_alonso_ortiz">
            <aside>
            <header>
                <img src="../img/team/eva_alonso_ortiz.jpg" style="height:200px; border-radius:50%;">
                <h3>Eva Alonso Ortiz</h3>
                <h4>OSR Co-chair</h4>
                <h6>Department of Electrical Engineering, Polytechnique Montreal</h6>
                <h4>
                <a target="_blank" href="https://twitter.com/EvaAlonsoOrtiz"><i class="fa fa-twitter fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                <a target="_blank" href="https://github.com/evaalonsoortiz"><i class="fa fa-github fa-2x" style="position: relative; top: 0px; text-indent:0px; vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                <a target="_blank" href="https://www.evaalonsoortiz.com/"><i class="fa fa-external-link-square fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                </h4>
                <br>
            </header>
            </aside>
            </a>
        </td>
        <td class="people">
            <a style="display:block; color:#05323F" href="../team_gabriel_gonzalez_escamilla">
            <aside>
            <header>
                <img src="../img/team/gabriel_gonzalez_escamilla.jpg" style="height:200px; border-radius:50%;">
                <h3>Gabriel González Escamilla</h3>
                <h4>OSR Co-chair</h4>
                <h6>Department of Neurology, University medical center of the Johannes Gutenberg University Mainz, Mainz</h6>
                <h4>
                <a target="_blank" href="https://twitter.com/NeuroGabriel"><i class="fa fa-twitter fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                <a target="_blank" href="https://github.com/GGonEsc"><i class="fa fa-github fa-2x" style="position: relative; top: 0px; text-indent:0px; vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                <a target="_blank" href="https://multimodalneuroimaging.wordpress.com/about/"><i class="fa fa-external-link-square fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                </h4>
                <br>
            </header>
            </aside>
            </a>
        </td>
    </tr>
</table>




### A special thanks to our volunteers!
<p align="justify">
Our call for volunteers to help build a great Open Science Room was met with enthusiasm! We now have multiple teams up and running and we're very excited about what's next. We are so grateful to be part of such an engaging and helpful community. Thank you all!
</p>
<p align="justify">
Together with the OSR team, the wonderfully talented and hard-working volunteers below made significant contributions to the Open Science Room. We have greatly enjoyed working with them, and proud to have them in our community.
Have a look at their contact links and bios below, and give them a virtual high-five in the OSR!
</p>
<br>


<html>

{% assign volunteers = site.volunteers %}

{% assign n_rows = volunteers.size | divided_by:2 %}
<table class="people">
{% for row in (0..n_rows) %}
    <tr class="people">
    {% for col in (0..1) %}
        <td class="people">

        {% assign idx = row | times:2 | plus:col %}
        {% assign person = volunteers[idx] %}
        {% if person %}

            {% assign img_path = nil %}
            {% assign names = person.Name | downcase | split: " " %}
            {% assign img_path = site.baseurl | append: "/img/person_default.jpg" %}
            {% for file in site.static_files %}                
                {% if file.path contains names.first and file.path contains names[1] %}
                    {% assign img_path = file.path %}
                {% endif %}
            {% endfor %}

            <a style="display:block; color:#05323F" href="{{ site.baseurl }}{{person.url}}">
            <aside class="speaker-card {% if speaker.column %} {{ speaker.column }}{% endif %}">
            <header>
                <img src="{{ site.baseurl }}{{ img_path }}" style="height:200px; border-radius:50%;">

                <h3>{{ person.Name }}</h3>

                <h6>{{ person.Affiliation }}</h6>

                <h4>
                {% if person.Twitter %} <a target="_blank" href="https://twitter.com/{{ person.Twitter }}"><i class="fa fa-twitter fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a> {% endif %}
                {% if person.Github %} <a target="_blank" href="https://github.com/{{ person.Github }}"><i class="fa fa-github fa-2x" style="position: relative; top: 0px; text-indent:0px; vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>{% endif %}
                {% if person.Website %} <a target="_blank" href="{{ person.Website }}"><i class="fa fa-external-link-square fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>{% endif %}
                </h4>
                <br>
            </header>
            </aside>
            </a>
        {% endif %}
        </td>
    {% endfor %}
    </tr>
{% endfor %}
</table>

</html>
