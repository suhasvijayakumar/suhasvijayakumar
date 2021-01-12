---
layout: main_page
title: academia
---
{% include toc.html %}

## Motivation and current position
You probably can't differentiate between flowers that are harmless, from the ones that can kill you in an instant. You probably also can't hang silently from a tree for hours on end, grooming you friends. Suffice to say that we've branched off of our closest ancestors and have managed to acquire different skills along the way like effectively communicating with someone, be it across the room, or across the ocean.

But how did our brains evolve to achieve such a feat? How are our brains different from other animals', from each others'? And just how does that result in the vast variety of behavior that we see - with some capable of composing beautifully complicated symphonies, and some others capable of reciting *pi* to a hundred decimal places?

I finished my PhD work at the [Cognitive Neuroecology Lab](http://www.rbmars.dds.nl/lab.html) of the Donders Institute, Nijmegen, where we studied the parietal-frontal networks using resting state functional connectivity. I was supervised by Dr. Rogier B. Mars and Prof. Dr. Pieter Medendorp. Currently, I work as a fellow at Harvard University in the [Evolutionary Neuroscience Lab](https://projects.iq.harvard.edu/evolutionaryneurosciencelab/home) led by Dr. Erin Hecht.

## Education & Work

**Post-doctoral fellow** | Evolutionary Neuroscience Lab | December, 2019 – present <br>
Evolutionary Neuroecology Lab <br>
Harvard University <small> Cambridge, MA, USA </small>

**PhD** | Cognitive Neuroscience | 2015 – 2019 <br>
Cognitive Neuroecology Lab <br>
Donders Institute for Brain, Cognition and Behaviour <small> Nijmegen, The Netherlands </small>

**M.Sc** | Cognitive Neuroscience | 2013 – 2015 <br>
Specialization: Brain Networks and Neuronal Communication <br>
Radboud University <small> Nijmegen, The Netherlands </small>

**B.Sc** | Physics, Maths, Electronics | 2009 – 2012 <br>
St. Joseph’s College <small> Bengaluru, India </small>

**Pre-University** | 2007 – 2009 <br>
Studied: Physics, Maths, Computer Science & Chemistry <br>
Sadvidya Composite Pre-University College <small> Mysuru, India</small>

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
