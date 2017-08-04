---
layout: default
title:  "Syllabus"
categories: schedule
lectures:
   -
    date: 2017-07-25
    title: Introduction; probability theory
    who: trevor
    slides: 01_intro_prob_theory.pdf
    reading: Bishop 1.1-1.2
    show: 1
   -
    date: 2017-07-27
    title: Probabilistic models and parameter fitting
    who: trevor
    slides: 02_statistical_schools.pdf
    reading: Bishop 2.1*, 2.3*; 1.2.3-1.2.4 (* = first 2 pages)
    show: 1
   -
    date: 2017-08-01
    title: Linear regression; Intro to regularisation
    who: andrey
    slides: 03_linear_regression.pdf
    reading: Bishop 3.1.1, 3.1.2, 3.1.4
    show: 1
   -
    date: 2017-08-03
    title: Logistic regression classifier; Basis expansion
    who: andrey
    slides: 04_logistic_regression.pdf
    reading: Bishop 4.3.2, 3.1*
    show: 1
   -
    date: 2017-08-08
    title: Iterative optimisation of loss functions; Model complexity and bias-variance analysis
    who: andrey
    slides: 05_optim_regularisation.pdf
    reading: Bishop 1.5.5, 3.2
    show: 1
   -
    date: 2017-08-10
    title: Notes on vectors; Perceptron classifier
    who: andrey
    slides: 06_vectors_perceptron.pdf
    reading: Bishop 4.1.7
    show: 1
   -
    date: 2017-08-15
    title: Non-linear models, using basis functions and Artificial Neural Networks
    who: andrey
   -
    date: 2017-08-17
    title: Artificial Neural Networks
    who: andrey
   -
    date: 2017-08-22
    title: Notes on linear algebra
    who: andrey
   -
    date: 2017-08-24
    title: Support Vector Machines
    who: andrey
   -
    date: 2017-08-29
    title: Support Vector Machines
    who: andrey
   -
    date: 2017-08-31
    title: Kernel Methods
    who: andrey
   -
    date: 2017-09-05
    title: Unsupervised learning
    who: andrey
   -
    date: 2017-09-07
    title: Unsupervised learning
    who: andrey
   -
    date: 2017-09-12
    title: Dimensionality reduction, principal component analysis
    who: andrey
   -
    date: 2017-09-14
    title: Multidimensional scaling, spectral clustering
    who: andrey
   -
    date: 2017-09-19
    title: Bayesian fundamentals
    who: trevor
   -
    date: 2017-09-21
    title: Bayesian inference with conjugate priors
    who: trevor
   -
    date: 2017-09-25
    title: Non-teaching week
   -
    date: 2017-10-03
    title: Probabilistic graphical models, fundamentals
    who: trevor
   -
    date: 2017-10-05
    title: Probabilistic graphical models, conditional independence 
    who: trevor
   -
    date: 2017-10-10
    title: Probabilistic graphical models, inference
    who: trevor
   -
    date: 2017-10-12
    title: Probabilistic graphical models, belief propagation
    who: trevor
   -
    date: 2017-10-17
    title: Probabilistic graphical models, statistical inference and applications
    who: trevor
   -
    date: 2017-10-19
    title: Subject review
    who: trevor
---

## Syllabus

We'll put the lecture slides in the week that we cover the material, as well as pointers to the required reading. 
Reading references to Bishop relate to the book *Pattern recognition and machine learning by Christopher M. Bishop, 2006.*
<p>

<table class="display">
<colgroup>
<col width="15%" />
<col width="35%" />
<col width="40%" />
</colgroup>
<thead>
<tr>
    <td><b>Date</b></td>
    <td><b>Topic</b></td>
    <td><b>Materials</b></td>
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

All materials Copyright 2017, The University of Melbourne, and should not be reproduced or distributed without permission.
