---
title: Social event
---

<div class="social-event">

  <p><br>
     The social event will take place from 18:00 to 22:00 at the <a href="https://www.securecodewarrior.com">Secure Code Warrior's</a> office at Baron Ruzettelaan 5 Bus 3, 8310 Brugge.<br />
     The link to register for the social event will be added soon.<br />
     Be aware of the following: <a href="https://www.vlaanderen.be/maatregelen-tijdens-de-coronacrisis">https://www.vlaanderen.be/maatregelen-tijdens-de-coronacrisis</a>.
  </p>

{% assign socialEventSponsors = site.data.sponsors | where:"level","Social event" | sort: 'name' %}

  {% if socialEventSponsors %}
    {% for sponsor in socialEventSponsors %}
      <div class="socialevensponsor">
        <a href="{{ sponsor.url }}"><img src="/assets/images/sponsors/{{ sponsor.image }}" alt="{{ sponsor.name }} logo" style="{{ sponsor.style }}"/></a><br />
      </div>
    {% endfor %}
  {% endif %}

</div>
