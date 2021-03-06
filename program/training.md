---
title: Trainings
---

<div align=center>
  <p>
    Register for a training at <a href="https://owasp-benelux-days-spring-2022.eventbrite.com">https://owasp-benelux-days-spring-2022.eventbrite.com</a>.<br/>
    <font color="#FF0000;">Registering for multiple trainings will result in a cancellation of all!</font>
  </p>
</div>

<div class="keynote-full">

{% if site.data.training[0].name %}
	<h1>Trainings on Thursday the 31st of March:</h1>
	<br />
	<ul>
	{% assign trainings = site.data.training | sort: 'name' %}
	{% for training in trainings %}
		{% if training.name %}
		<li>
        <a name="{{training.name | replace: " ","-"}}">
        <img style="background-image: url(/assets/images/training/{{training.image | default:'owasp_logo.png'}});{{training.style}};"></a>
      {% if training.title %}
        <h2>{{training.title}} by {{training.name}}</h2>
      {% else %}
        <h2>{{training.name}}</h2>
      {% endif %}

      {% if training.feed %}
        <p>
          <a href="/program/feeds#{{training.name}}">Check out the streaming feed!</a>
        </p>
      {% endif %}

      {% if training.abstract %}
        <h4>Abstract:</h4>
          <p>{{training.abstract}}</p>
          <br>
      {% endif %}
      {% if training.bio %}
        <h4>Bio:</h4>
	<p>{{training.bio}}</p>
        <br>
      {% endif %}
		</li>
		{% endif %}
	{% endfor %}
	</ul>
{% else %}
  <p><br>
     We're currently in the progress of making the training schedule.<br>
     We will share the information very soon.
  </p>
{% endif %}
</div>
