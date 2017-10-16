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
    title: Artificial Neural Networks
    who: andrey
    slides: 07_backpropagation.pdf
    reading: Bishop 5.1, 5.2, 5.3
    show: 1
   -
    date: 2017-08-17
    title: Artificial Neural Networks (cont.)
    who: andrey
    slides: 08_convnet_autoenc.pdf
    reading: Bishop 5.5.6
    show: 1
   -
    date: 2017-08-22
    title: Support Vector Machines (hard margin)
    who: andrey
    slides: 09_hard_margin_svm.pdf
    reading: Bishop 7.1
    show: 1
   -
    date: 2017-08-24
    title: Support Vector Machines (soft margin)
    who: andrey
    slides: 10_soft_margin_svm.pdf
    reading: Bishop 7.1.1
    show: 1
   -
    date: 2017-08-29
    title: Kernel Methods
    who: andrey
    slides: 11_kernel_methods.pdf
    reading: Bishop 6.2
    show: 1
   -
    date: 2017-08-31
    title: Ensemble Learning; Interim Summary
    who: andrey
    slides: 12_ensemble_revision.pdf
    reading: Bishop 14.2
    show: 1
   -
    date: 2017-09-05
    title: Unsupervised Learning; Clustering
    who: andrey
    slides: 13_clustering_gmm.pdf
    reading: Bishop 9.1, 9.2
    show: 1
   -
    date: 2017-09-07
    title: Expectation Maximisation Algorithm
    who: andrey
    slides: 14_em_algorithm.pdf
    reading: Bishop 9.4, 9.2.2
    show: 1
   -
    date: 2017-09-12
    title: Principal Component Analysis; Multidimensional Scaling
    who: andrey
    slides: 15_dimred_pca_mds.pdf
    reading: Bishop 12.1, 12.4.3, Hastie 14.8
    show: 1
   -
    date: 2017-09-14
    title: Manifold Learning; Spectral clustering
    who: andrey
    slides: 16_manifold_learning.pdf
    reading: Bishop 12.4.3, Hastie 14.5.3, 14.9
    show: 1
   -
    date: 2017-09-19
    title: Bayesian inference
    who: trevor
    slides: 17_bayesian_inference.pdf
    reading: Bishop 2.3.6, 4.4-4.5
    show: 1
   -
    date: 2017-09-21
    title: Bayesian inference (cont.)
    slides: 18_bayesian_classification.pdf
    reading: Bishop 2.1, 3.3, 3.4
    who: trevor
    show: 1
   -
    date: 2017-09-25
    title: Non-teaching week
   -
    date: 2017-10-03
    title: Probabilistic graphical models, fundamentals
    who: trevor
    slides: 20_pgm_basics.pdf
    reading: Bishop 8-8.3.1
    show: 1
   -
    date: 2017-10-05
    title: Probabilistic graphical models, independence 
    who: trevor
    slides: 21_pgm_indy.pdf
    reading: Bishop 8.2-8.3.2
    show: 1
   -
    date: 2017-10-10
    title: Probabilistic graphical models, inference
    who: trevor
    slides: 22_pgm_elimination.pdf
    reading: Russell and Norvig Chapter 14 (see "Reading" on LMS) or Murphy 20.3
    show: 1
   -
    date: 2017-10-12
    title: Probabilistic graphical models, statistical inference.  Lecture cancelled, please listen to 2016 recording available under LMS in the reading/resources option.
    who: trevor
    slides: 23_pgm_stat_infer.pdf
    reading: Murphy 11.4.4 (generally dip into 11.3-11.4)
    show: 1
   -
    date: 2017-10-17
    title: Probabilistic graphical models, hidden Markov models and message passing
    who: trevor
    slides: 24_pgm_message_passing.pdf
    reading: Murphy 17 (mainly 17.4-17.5)
    show: 1

   -
    date: 2017-10-19
    title: Subject review
    who: trevor
---

## Syllabus

We'll put the lecture slides in the week that we cover the material, as well as pointers to the required reading. 
Reading references to Bishop relate to the book *Pattern recognition and machine learning by Christopher M. Bishop, 2006.*
Reading references to Murphy relate to the book <a href="https://ebookcentral.proquest.com/lib/UNIMELB/reader.action?docID=3339490&ppg=1">Machine Learning : A Probabilistic Perspective by Kevin Murphy, 2014;</a> available in electronic ebook form using the link. 
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
