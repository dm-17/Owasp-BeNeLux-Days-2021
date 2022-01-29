---
title: Social event
---

<div class="social-event">

  <p><br>
    TBD
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
