---
layout: kz-frontpage
permalink: /index.html
homepage: true
homepage_title: Samudra<br>is a system accelerator. 
homepage_teaser: Similar to how a startup accelerator works with startups to turn them into successful companies, a system accelerator works with organisations with relevant capacities to turn a dysfunctional/nonexistent system into a functional one. 
title: Samudra
header: no
skip_boilerplate: yes

---

We wanted to build an organisation that solves global challenges by building functional systems, without becoming part of those systems, and hence without adding more complexity. Since we found no existing template for this type of organisation, we came up with the term "system accelerator". We believe that an organisation of this type can achieve fast progress on global challenges like climate change, environmental degradation and health - challenges where involvement of many different types of stakeholders is necessary, and where everyone benefits once the goal is achieved but the financial incentives are not aligned with achieving the goal. 

<footer id="footer-content" class="bg-grau">
  <div id="footer">
  	<nav class="row">
      <section class="columns">
        <p>
        </p>
      </section>
    </nav>
  	<nav class="row">
      <section class="columns">
        <p>
        </p>
      </section>
    </nav>
    <nav class="row">
      <section class="columns social-icons">
        <!-- div to centre icons -->
        <div>
          <ul class="inline-list">
            {% for social_item in site.data.socialmedia %}
            <li><a href="{{ social_item.url }}" target="_blank" class="{{ social_item.class }}"
                   title="{{ social_item.title }}"></a></li>
            {% endfor %}
          </ul>
        </div>
      </section>
    </nav>
    <nav class="row">
      <section class="columns">
        <p>
          &#169; Copyright 2020-2023 Samudra.world. All rights reserved. This website does not use cookies.
        </p>
      </section>
    </nav>
  </div>
</footer>

<script>
  // Ensure that all external links open in new tabs
  var links = document.links;
  for (var i = 0, linksLength = links.length; i < linksLength; i++) {
     if (links[i].hostname != window.location.hostname) {
         links[i].target = '_blank';
     }
  }
</script>

<script src="/assets/js/javascript.min.js"></script>
<script src="/assets/js/karina.js"></script>
