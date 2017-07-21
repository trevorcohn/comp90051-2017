---
layout: lean
title:  "Syllabus"
date:   2017-05-10 11:21:00 +1000
categories: schedule
lectures:
   -
    date: 2017-07-24
    title: Introduction 
    who: trevor
    slides: sample_slides.pdf
    show: 1
   -
    date: 2017-07-24
    title: Probabilistic models and parameter fitting
    who: trevor
    slides: sample_slides2.pdf
    show: 0
   -
    date: 2017-07-31
    title: Linear models, fundamentals and regression
    who: andrey
   -
    date: 2017-07-31
    title: Linear models, regularisation and logistic regression classifier
    who: andrey
   -
    date: 2017-08-07
    title: Optimisation of loss functions and gradient methods
    who: andrey
   -
    date: 2017-08-07
    title: Perceptron classifier
    who: andrey
   -
    date: 2017-08-14
    title: Non-linear models, using basis functions and Artificial Neural Networks
    who: andrey
   -
    date: 2017-08-14
    title: Artificial Neural Networks
    who: andrey
   -
    date: 2017-08-21
    title: Support Vector Machines
    who: andrey
   -
    date: 2017-08-21
    title: Support Vector Machines
    who: andrey
   -
    date: 2017-08-28
    title: Semi-supervised learning and ensembles
    who: andrey
   -
    date: 2017-08-28
    title: Midsemester test
    who: andrey
   -
    date: 2017-09-04
    title: Unsupervised learning
    who: andrey
   -
    date: 2017-09-04
    title: Unsupervised learning
    who: andrey
   -
    date: 2017-09-11
    title: Dimensionality reduction, principal component analysis
    who: andrey
   -
    date: 2017-09-11
    title: Multidimensional scaling, spectral clustering
    who: andrey
   -
    date: 2017-09-18
    title: Bayesian fundamentals
    who: trevor
   -
    date: 2017-09-18
    title: Bayesian inference with conjugate priors
    who: trevor
   -
    date: 2017-09-25
    title: Non-teaching week
   -
    date: 2017-10-02
    title: Probabilistic graphical models, fundamentals
    who: trevor
   -
    date: 2017-10-02
    title: Probabilistic graphical models, conditional independence 
    who: trevor
   -
    date: 2017-10-09
    title: Probabilistic graphical models, inference
    who: trevor
   -
    date: 2017-10-09
    title: Probabilistic graphical models, belief propagation
    who: trevor
   -
    date: 2017-10-16
    title: Probabilistic graphical models, statistical inference and applications
    who: trevor
   -
    date: 2017-10-16
    title: Subject review
    who: trevor
---

## Syllabus

We'll put the lecture slides in the week that we cover the material, as well as pointers to the required reading. 

Lectures are on Tuesdays and Thursdays, as described in the <a href="https://sws.unimelb.edu.au/2017/Reports/List.aspx?objects=COMP90051&weeks=1-52&days=1-7&periods=1-56&template=module_by_group_list">timetable</a>. Note that workshops will run from week 2 until the end of semester. There will also be an office hour each week, run immediately after the Thursday lecture, 1-2pm in DMD 7.03.

All materials are Copyright 2017, The University of Melbourne, and should not be reproduced or distributed without permission.
<p>

<table class="display">
<colgroup>
<col width="15%" />
<col width="35%" />
<col width="40%" />
</colgroup>
<thead>
<tr>
    <td>Date</td>
    <td>Topic</td>
    <td>Materials</td>
</tr>
</thead>
<tbody>
{% for lect in page.lectures %}
<tr>
  <td>
    {% if lect.type == "workshop" %}
        from
    {% endif %}
       {{ lect.date  | date: "%a %-d/%-m" }}
  </td>
  <td><i>{{ lect.title }}</i>
    {% for matter in lect.materials %}
    <br> {{ matter }}
    {% endfor %}
  </td>
  <td>
    {% if lect.show == 1 %}
        {% if lect.slides %}
            <b>Slides: </b>
            {% assign first = 1 %}
            {% for matter in lect.slides %}
                {% if first == 1 %}
                    {% assign first = 0 %}
                {% else %}
                    <br> &nbsp;
                {% endif %}
                <a href="slides/{{ matter }}">{{ matter }}</a>
            {% endfor %}
            <br>
        {% endif %}
        {% if lect.worksheet %}
            <b>Worksheet: </b>
            {% assign first = 1 %}
            {% for matter in lect.worksheet %}
                {% if first == 1 %}
                    {% assign first = 0 %}
                {% else %}
                    <br> &nbsp;
                {% endif %}
                <a href="workshops/{{ matter }}">{{ matter }}</a>
            {% endfor %}
            <br>
        {% endif %}
        {% if lect.reading %}
            <b>Reading: </b>
            {% assign first = 1 %}
            {% for matter in lect.reading %}
                {% if first == 1 %}
                    {% assign first = 0 %}
                {% else %}
                    <br> &nbsp;
                {% endif %}
                {{ matter }}
            {% endfor %}
            <br>
        {% endif %}
        {% if lect.notebook %}
            <b>Notebook: </b>
            {% assign first = 1 %}
            {% for matter in lect.notebook %}
                {% if first == 1 %}
                    {% assign first = 0 %}
                {% else %}
                    <br> &nbsp;
                {% endif %}
                <a href="notebooks/{{ matter }}">{{ matter }}</a>
            {% endfor %}
            <br>
        {% endif %}
    {% endif %}

     {% if lect.show == 2 %}
        {% if lect.reading %}
            <b>Reading: </b>
            {% assign first = 1 %}
            {% for matter in lect.reading %}
                {% if first == 1 %}
                    {% assign first = 0 %}
                {% else %}
                    <br> &nbsp;
                {% endif %}
                {{ matter }}
            {% endfor %}
            <br>
        {% endif %}
       {% endif %}

  </td>
</tr>
{% endfor %}
</tbody>
</table>
