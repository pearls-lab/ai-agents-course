---
title: CSE 291 - AI Agents - UCSD CSE
layout: default
img: # heroes_journey.png
active_tab: main_page 
---

<!--
<div class="alert alert-warning" markdown="1">
Want to join the class, but didn't attend the first lecture? Here are the steps to follow:
1. [Get a permit by signing yourself up for CIS 700-001 via the waitlist system](https://forms.cis.upenn.edu/waitlist/index.php).  
2. [Do the for-credit in-class assignment from the first lecture](http://interactive-fiction-class.org/in_class_activities/play-text-adventures/play-text-adventures.html).
3. [Listen to recording of the first lecture](https://upenn.hosted.panopto.com/Panopto/Pages/Sessions/List.aspx?folderID=8b5f2734-0738-4f52-90f5-ab3c01236b7c) and [look over the slides](http://interactive-fiction-class.org/slides/text-adventure-games.pdf).
4. [Complete the first homework assignment before class on Thursday](http://interactive-fiction-class.org/homeworks/text-adventure-game/text-adventure-game.html).
</div>
-->

<!--
<div class="alert alert-success" markdown="1">
[Post your game here.](https://docs.google.com/document/d/1XpBEevYpHvLjCr-3CkAhERN_GPHsjNmkPo-Wf9KjxDs/edit?usp=sharing)
</div>
-->

<!-- Display an alert about upcoming homework assignments -->
{% capture now %}{{'now' | date: '%s'}}{% endcapture %}
{% for page in site.pages %}
{% if page.release_date and page.due_date %}
{% capture release_date %}{{page.release_date | date: '%s'}}{% endcapture %}
{% capture due_date %}{{page.due_date | date: '%s'}}{% endcapture %}
{% if release_date < now and due_date >= now %}
{% if page.type == "in-class" %}
<!-- In class activity -->
<div class="alert alert-danger">
The in-class activity for {{ page.release_date | date: "%A %b %-d" }} will be to <a href="{{page.url}}">{{ page.title }}</a>.  
</div>
<!-- Other participation activity -->
{% elsif page.type == "participation" %}
<div class="alert alert-info">
The participation activity <a href="{{page.url}}">{{ page.title }}</a> is due on {{ page.due_date | date: "%A, %B %-d, %Y" }} before {{ page.due_date | date: "%I:%M%p" }}. 
</div>
{% else %}
<!-- Homework assignment -->
<div class="alert alert-success">
<a href="{{page.url}}">{{page.type}} {{page.number}}: {{page.title}}</a> has been released.  
{% if page.deliverables %}
The assignment has multiple deliverables.
<ul>
{% for deliverable in page.deliverables %}
<li>{{ deliverable.due_date | date: "%b %-d, %Y" }} - {{deliverable.description}}.</li>
{% endfor %}
</ul>
{% else %}
It is due before {{ page.due_date | date: "%I:%M%p" }} on {{ page.due_date | date: "%A, %B %-d, %Y" }}.
{% endif %}
</div>
{% endif %}
{% endif %}
{% endif %}
{% endfor %}
<!-- End alert for upcoming homework assignments -->


<!--
<div class="alert alert-success" markdown="1">
A great example of what you could build if you take this class is the [AI Dungeon](https://play.aidungeon.io/), which is an interactive fiction game  that was developed by a student at BYU using [Open AI's GPT-2](https://openai.com/blog/better-language-models/) large scale language model.
</div>
-->
<!--
<div class="alert alert-success" markdown="1">
First day of class is Thursday, January 13, 2022 at 1:45pm-3:15pm Eastern. It will take place virtually. Here is the [Zoom link](https://upenn.zoom.us/j/95868341588?pwd=a0NvbkhtUEdYTTk5d0Vmc2VvcHJrUT09). We look forward to seeing you there!
</div>
-->

Course number
: CSE 291 - AI Agents

Course Description: This course will cover the basics of (1) what LLM-based AI Agents actually are; (2) where they can be useful (and where they are not); and (3) how to safely train and deploy an agent for a given virtual domain.

Required Knowledge: Students should be familiar with basic CS concepts such as Search (A*, Monte Carlo Tree Search) and Deep Learning concepts such as Transformers (how self-attention works) and the basics of how Large Language Models are (pre-)trained. Students are expected to come into the class with the ability to implement these concepts from scratch (in Python/numpy) and also be able to use popular libraries such as Huggingface. Basic knowledge of Reinforcement Learning (what is a Markov Decision Process, differences between online and offline RL, RL from Human Feedback) is a plus but not required.

Recommended Preparation for Those Without Required Knowledge: Undergrad Intro to AI/RL, and grad level Intro to Deep Learning / NLP types of courses are highly recommended

Website
: [pearls-lab.githib.io](http://interactive-fiction-class.org/)

Instructors
: [Prithviraj Ammanabrolu](https://prithvirajva.com)

TAs
: [Bosung Kim](https://bosung.github.io)

Time and Place
: Winter 2024, Tuesdays & Thursdays from 3:30 to 4:50 pm PT in CSE 2154
: First day of class is January 06, 2025
: Last day of class is

Office Hours (see the [Staff](/staff.html) page for office hour locations)

Course Materials
: There is no textbook for this course, but you will be required to puchase a varitey of materials including software and API credits. If any of these are prohibitively expensive for your budget, please let the instructor know.

<!-- Games
: [Labyrinth The Adventure Game](https://www.amazon.com/Jim-Hensons-Labyrinth-Adv-Game/dp/1916011551/) - $35 on Amazon
: [Action Castle](http://www.memento-mori.com/pdf/parsely-preview-n-play-edition) - Free (you can optionally buy it in the rad [Parsley book in print](http://www.memento-mori.com/books/parsely-book) or [PDF](http://www.memento-mori.com/pdf/parsely-pdf)) - $20-30 -->


<!-- Materials 
: [ChatGPT Plus subcription](http://chat.openai.com) - $20/month -->


Grading

Paper Presentations
: Over the course of the semester, each student must prepare one or more 10-15 minute presentations on a research paper relevant to the course. Since these presentation will be a substantial component of the learning experience in the class, slides must be prepared and emailed to us at least 72 hours in advance of the lecture they will be presented in (e.g., by 3PM on the Monday before the presenation date), so that we can provide feedback on them. Failure to send us the slides ahead of time will result in a grade penalty on the presentation. 

Collaboration Policy
: Homeworks are expected to be done individually, and teams of ~5 are needed for the final project.

Late Day Policy
: Each student has five free "late days".  Homeworks can be submitted at most two days late.  If you are out of late days, then you will not be able to get credit for subsequent late assignments. One "day" is defined as anytime between 1 second and 24 hours after the homework deadline. The intent of the late day policy it to allow you to take extra time due to unforseen circumstances like illnesses or family emergencies, and for forseeable interruptions like on campus interviewing and religious holidays.  You do not need to ask permission to use your late days.  No additional late days are granted. **Late days only apply to the homeworks. They cannot be used on the final project, which must be finished by the final day of class.  Late days may not be used for paper presentations.**