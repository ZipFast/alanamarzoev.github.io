---
title: Alana Marzoev
layout: home
---

<table border="0" cellpadding="0">
<td valign="top" style="min-width:250px;">
<img src="/assets/hiking.png" width="250">
</td>
</table>


I am a computer science PhD student at MIT, supported by a Jacobs Presidential fellowship. I’m interested in natural language processing and data systems. ]

I am extremely fortunate to be coadvised by Samuel Madden, Jacob Andreas, and Frans Kaashoek, and to work closely with Mike Cafarella. 

Before I came to MIT, I was an undergraduate at Cornell University. During my time there,  I explored the implications of resource disaggregation in the cloud,  investigated the effects of low precision arithmetic and variance reduction on the performance and hardware efficiency of stochastic gradient descent (SGD), and led a team of 50+ engineers in designing and building a fully-functional prototype of a Hyperloop pod. 

I’ve had the opportunity to do many wonderful summer internships, including spending a summer at UC Berkeley’s RISELab, where I worked on Ray,  a distributed execution engine for machine learning, and another working on computer vision problems at a 3D bioprinting startup, Allevi. I also spent a fantastic six months at Microsoft Research in Cambridge, U.K, where I was a part of the Cloud Infrastructure team. I worked as a networking intern on Project Sirius, and as a deep learning intern on Project Silica. 


<h2 class="tableheading">Publications</h2>

<table border="0">
  {% for pub_keyval in site.data.publications %}
    <tr>
      {%- assign pub = pub_keyval[1] -%}
      <td>
        <b><a href="{{pub_keyval[0]}}.html" style="color: #464646">{{ pub.title }}</a></b><br/>
        {%- for author in pub.authors -%}
          {%- if forloop.last == true and forloop.length > 1 %}
            and
          {%- endif %}
          {%- if author == "marzoev" %}
            <font color="#000000">{{ site.data.authors[author].name }}</font>
          {%- else %}
            <a href="{{- site.data.authors[author].site -}}" style="color: #464646">{{ site.data.authors[author].name }}</a>
          {%- endif -%}
          {%- if forloop.last == false and forloop.length > 2 -%}
            ,
          {%- endif %}
        {%- endfor -%}<br/>
        <i>{{ pub.venue }}
        {%- if pub.venuenote %}
        ({{ pub.venuenote }})
        {%- endif -%}
        {%- if pub.volume -%}
        , Volume {{ pub.volume }}
        {%- endif -%}
        {%- if pub.issue -%}
        , Issue {{ pub.issue }}
        {%- endif -%}
        </i>, {{ pub.month }} {{ pub.year }}<br/>
        {%- if pub.award -%}
          <i><b>{{ pub.award }}</b></i><br/>
        {%- endif -%}
      </td>
      <td valign="top" width="20">
        {% if pub.pdf %}
          <a href="{{ pub.pdf }}"><img src="/assets/pdf.png" alt="pdf" /></a>
        {% endif %}
        {% if pub.movie %}
          <a href="{{ pub.movie }}"><img src="/assets/movie.png" alt="youtube" /></a>
        {% endif %}
      </td>
    </tr>
{% endfor %}
</table>


<h2 class="tableheading">Press</h2>

<table border="0">
{%- for press_keyval in site.data.press %}
  {%- assign press= press_keyval[1] -%}
  <tr>
  <td> 
    <b><a href="{{press.url}}">{{press.title}}</a></b><br/>{{press.venue}}
  </td>
  </tr>
{% endfor %}
</table>

