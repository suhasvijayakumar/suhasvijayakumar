---
layout: main_page
title: academia
---
{% include toc.html %}

## Motivation and current position
For the most part of my career in the field of neuroscience, 
I genuinely found joy in comparing brains of various species 
to understand what aspects of the structure of the brain set them apart. 
Questions in the field of evolutionary neuroscience mostly stem from curiosity, 
from the need to understand something deeply and lay out the nuances. 
But during the course of my first postdoc, in the middle of the Covid-19 pandemic, 
I realised that curiosity alone was not enough to sustain my motivation for work. 
I wanted to work on something that had a clear path between research and its application in the world. 

After months of discussions with experts in the field of ultrasonic neuromodulation, 
cold emails to leading researchers, lunches with PhD students in the field, and some more reconsiderations, 
I decided to start work in the (relatively new) field of low-intensity focused ultrasound neuromodulation. 
Currently, as a postdoc in the Neurostimulation Group of Prof. Dr. Til Ole Bergmann, 
I am using my background in physical sciences and neuroimaging to understand 
the effects of focused ultrasound stimulation starting with healthy population. 
Eventually, we hope to be able to use this technique 
in supporting people with neurological disorders. 

## Education & Work

**Post-doctoral fellow** | Neurostimulation Group | April, 2023 – present <br>
University Medical Center of the Johannes Gutenberg University Mainz <small> Mainz, Germany </small>

**Post-doctoral research fellow** | Evolutionary Neuroscience Lab | 2019 – 2022 <br>
Harvard University <small> Cambridge, MA, USA </small>

**PhD** | Cognitive Neuroecology Lab | 2015 – 2019 <br>
 Title: Principles of parietal-frontal cortical organization.<br>
Donders Institute for Brain, Cognition and Behaviour <small> Nijmegen, The Netherlands </small>

**M.Sc** | Cognitive Neuroscience | 2013 – 2015 <br>
Specialization: Brain Networks and Neuronal Communication <br>
Radboud University <small> Nijmegen, The Netherlands </small>

**B.Sc** | Physics, Maths, Electronics | 2009 – 2012 <br>
St. Joseph’s College <small> Bengaluru, India </small>

## Publications
{% assign publications = site.data.publications %}
<ul reversed>
{% for pub in site.data.publications %}
    <li>
      <b>{{ pub.title }}</b> ({{ pub.year }}{% if pub.notes %}
       | <abbr>{{ pub.notes }}</abbr>{% endif %})
      <small>{{ pub.authors | join: '; ' }}</small>
      {{ pub.journal }} <i>{{ pub.volume }}</i>
      {% if pub.doi %}<br>
      [<a class="fa fa-link"></a> <a target="_blank" href="{{ pub.doi }}"> doi </a>]{% endif %} <br><br>
    </li>
{% endfor %}
</ul>
