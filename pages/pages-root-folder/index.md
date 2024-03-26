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

<!-- 
<a href="/goals/" target="_self" class="button radius">See what goals we are working on</a>
<a href="/goals/" target="_self" class="button radius">Learn more about our approach</a> 
-->

# How we operate

#### 1. Identify organisations with relevant capacities

<img src="/images/ops1.jpg">


#### 2. Understand why they operate the way they do

<img src="/images/ops2.jpg">

#### 3. Build a functional system (internal changes + powerful coordination)

<img src="/images/ops3.jpg">


# Our values

1. Climate<br> ...................

2. Environment<br> ...................

3. Health<br> ...................



# Our goals
<img src="/images/waste.jpg">
#### Building waste management systems in areas which lack waste collection services
10% of global emissions are related to waste, and these 10% get the least attention, so there are many low hanging fruits. 1 in 3 people globally don't have access to waste collection services. Most of them live in Asia, the most densely populated continent, and Africa, the youngest continent and hence most likely to experience population growth. These facts inspired Samudra's first goal - creating waste management systems in parts of Asia and Africa which lack waste collection services.


# How is a system accelerator different from other types of organisations

...................

...................


<footer id="footer-content" class="bg-grau">
  <div id="footer">
  	<nav class="row">
      <section class="columns">
        <p>
          Samudra is a system accelerator. Similar to how a startup accelerator works with startups to turn them into successful companies, a system accelerator works with organisations with relevant capacities to turn a dysfunctional/nonexistent system into a functional one. 
        </p>
      </section>
    </nav>
  	<nav class="row">
      <section class="columns">
        <p>
         Contact us:<br>
         We'd love to hear from you if your organisation also doesn't fit into buckets: hello@samudra.world<br>
         If you can help us with our exusting goals: goals@samudra.world<br>
         To pitch us a new goal in line with our values: new@samudra.world<br>
         If you'd like to work with us: team@samudra.world<br>
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
