---
layout: articles
title: Team
permalink: team/
---
<style>
  i {
    color: #555555;
    font-size: 14px;
  }

  p {
    line-height: 120%;
    margin: 0;
  }

  /* Additional styles for overlays */
  .overlay {
    color: white; /* Sets all text within the overlay to white */
    background-color: rgba(0, 0, 0, 0.5); /* Adds a semi-transparent black background to the overlay */
    padding: 10px; /* Adds padding around the text for better spacing */
  }
  
  .overlay--bottom {
    position: absolute;
    bottom: 0;
    width: 100%; /* Ensures the overlay covers the entire width of the image */
  }

  /* Ensure the card positioning context */
  .card {
    position: relative;
    overflow: hidden; /* Keeps the overlay within the boundaries of the card */
  }

  .card__image img {
    width: 100%; /* Ensure the image fills the container */
    height: auto; /* Maintain aspect ratio */
    object-fit: cover; /* Cover the container without stretching */
  }

.card__image a {
    display: block; /* Treat the link like a block element to fill the container */
  }

</style>


<div class="article-list grid grid--sm grid--p-3">
  <div class="cell cell--12 cell--md-4 cell--lg-3">
    <div class="card card--flat">
      <div class="card__image">
        <img class="image" src="/assets/images/teampic/dinesh.jpg" />
            <div class="overlay overlay--bottom">
              <header>
                <p><a href="https://dineshb-ucsd.github.io/">Dinesh Bharadia</a></p>
                <p><i style="color: #dddddd">Principal Investigator, Associate Professor ECE</i></p>
              </header>
            </div>
      </div>
    </div>
  </div>
  <div class="cell cell--12 cell--md-4 cell--lg-3">
    <div class="card card--flat">
      <div class="card__image">
        <img class="image" src="/assets/images/teampic/fred.jpg" />
            <div class="overlay overlay--bottom">
              <header>
                <p><a href="https://en.wikipedia.org/wiki/Fredric_J._Harris">Fred Harris</a></p>
                <p><i style="color: #dddddd">Honorable Member, Adjunct Professor ECE</i></p>
              </header>
            </div>
      </div>
    </div>
  </div>
</div>


<h3>PhD Students</h3>
<div class="article-list grid grid--sm grid--p-3">
  {% for people in site.data.people %}
    {% if people.role == "PhD" %}
      <div class="cell cell--12 cell--md-4 cell--lg-3">
        <div class="card card--flat">
          <div class="card__image">
                <img class="image" src="{{ people.picture }}" alt="Profile image of {{ people.name }}" />
            <div class="overlay overlay--bottom">
              <header>
              {% if people.website %}
                <p><a href="{{ people.website }}">{{ people.name }}</a></p>
              {% else %}
                <p>{{ people.name }}</p>
              {% endif %}
                <p><i style="color: #dddddd">{{ people.role }}</i></p>
              </header>
            </div>
          </div>
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div>


<h3>Collaborations and Postdoctoral Researchers</h3>
<div class="article-list grid grid--sm grid--p-3">
{% for people in site.data.people %}
  {% if people.role != "PhD" and people.role != "Principal Investigator" %}
   <div class="cell cell--12 cell--md-4 cell--lg-3">
      <div class="card card--flat">
        <div class="card__image">
            <img class="image" src="{{ people.picture }}" alt="Profile image of {{ people.name }}" />
          <div class="overlay overlay--bottom">
            <header>
              {% if people.website %}
                <p><a href="{{ people.website }}">{{ people.name }}</a></p>
              {% else %}
                <p>{{ people.name }}</p>
              {% endif %}
              <p><i style="color: #dddddd">{{ people.role }}</i></p>
            </header>
          </div>
        </div>
      </div>
    </div>
  {% endif %}
{% endfor %}
</div>


<div>
  <h3>Masters Students</h3>
  <div class="row">
    <div class="column">
      {% for people in site.data.people_text %}
        {% if people.role == "MS" %}
          {% if people.col == 1 %}
            <p style="line-height: 150%">{{ people.name }}</p>
          {% endif %}
        {% endif %}
      {% endfor %}
    </div>
    <div class="column">
      {% for people in site.data.people_text %}
        {% if people.role == "MS" %}
          {% if people.col == 2 %}
            <p style="line-height: 150%">{{ people.name }}</p>
          {% endif %}
        {% endif %}
      {% endfor %}
    </div>
  </div>
  <h3>Undergraduate Students</h3>
  <div class="row">
    <div class="column">
      {% for people in site.data.people_text %}
        {% if people.role == "BS" %}
          {% if people.col == 1 %}
            <p style="line-height: 150%">{{ people.name }}</p>
          {% endif %}
        {% endif %}
      {% endfor %}
    </div>
    <div class="column">
      {% for people in site.data.people_text %}
        {% if people.role == "BS" %}
          {% if people.col == 2 %}
            <p style="line-height: 150%">{{ people.name }}</p>
          {% endif %}
        {% endif %}
      {% endfor %}
    </div>
  </div>
<h3>Alumni</h3>
<h4>PhD</h4>
<div class="article-list grid grid--sm grid--p-3">
  {% assign alumni_with_pics = site.data.alumni | where_exp: "item", "item.picture" %}
  {% assign alumni_without_pics = site.data.alumni | where_exp: "item", "item.picture == nil" %}

  <!-- Alumni with Pictures -->
  {% for people in alumni_with_pics %}
    {% if people.role == "PhD" %}
      <div class="cell cell--12 cell--md-4 cell--lg-3">
        <div class="card card--flat">
            <div class="card__image">
              <img class="image" src="{{ people.picture }}" />
              <div class="overlay overlay--bottom" style="color: white;">
                <header>
                  {% if people.website %}
                    <p><a href="{{ people.website }}">{{ people.name }}</a></p>
                  {% else %}
                    <p>{{ people.name }}</p>
                  {% endif %}
                  <p><i style="color: white">Class of {{ people.year }}{% if people.now %}, {{ people.now }}{% endif %}</i></p>
                </header>
              </div>
            </div>
        </div>
      </div>
    {% endif %}
  {% endfor %}

  <!-- Alumni without Pictures -->
  <div class="list-group">
    {% for people in alumni_without_pics %}
      {% if people.role == "PhD" %}
        <div class="cell cell--12 cell--md-4 cell--lg-3">
          <div class="card card--flat">
              <div class="card__image-placeholder">
                <div class="placeholder-content">
                  {% if people.website %}
                    <p><a href="{{ people.website }}">{{ people.name }}</a></p>
                  {% else %}
                    <p>{{ people.name }}</p>
                  {% endif %}
                  <p><i>Class of {{ people.year }}{% if people.now %}, {{ people.now }}{% endif %}</i></p>
                </div>
              </div>
          </div>
        </div>
      {% endif %}
    {% endfor %}
  </div>
</div>

 
<h4>Postdocs and Researchers</h4>
<div class="article-list grid grid--sm grid--p-3">
  {% assign alumni_with_pics = site.data.alumni | where_exp: "item", "item.picture" %}
  {% assign alumni_without_pics = site.data.alumni | where_exp: "item", "item.picture == nil" %}

  {% for people in alumni_with_pics %}
    {% if people.role == "Visiting Researcher" or people.role == "Postdoc" %}
      <div class="cell cell--12 cell--md-4 cell--lg-3">
        <div class="card card--flat">
          <div class="card__image">
            <img class="image" src="{{ people.picture }}" />
            <div class="overlay overlay--bottom" style="color: white;">
              <header>
                  {% if people.website %}
                    <p><a href="{{ people.website }}">{{ people.name }}</a></p>
                  {% else %}
                    <p>{{ people.name }}</p>
                  {% endif %}
                <p><i style="color: white">{{ people.role }}{% if people.now %}, {{ people.now }}{% endif %}</i></p>
              </header>
            </div>
          </div>
        </div>
      </div>
    {% endif %}
  {% endfor %}
  <div class="list-group">
    {% for people in alumni_without_pics %}
      {% if people.role == "Researcher" or people.role == "Postdoc" %}
        <div class="cell cell--12 cell--md-4 cell--lg-3">
          <div class="card card--flat">
            <div class="card__image-placeholder">
              <div class="placeholder-content">
                  {% if people.website %}
                    <p><a href="{{ people.website }}">{{ people.name }}</a></p>
                  {% else %}
                    <p>{{ people.name }}</p>
                  {% endif %}
                <p><i>{{ people.role }}{% if people.now %}, {{ people.now }}{% endif %}</i></p>
              </div>
            </div>
          </div>
        </div>
      {% endif %}
    {% endfor %}
  </div>
</div>



<div class="row">
  <h4>Masters</h4>
  <div class="column">
    {% for people in site.data.alumni %}
      {% if people.role == "MS" %}
        {% if people.col == 1 %}
          <div class="row">
                {% if people.website %}
                  <p><a href="{{ people.website }}">{{ people.name }}</a></p>
                {% else %}
                  <p>{{ people.name }}</p>
                {% endif %}
            <p><i> Class of {{ people.year }}{% if people.now %}, {{ people.now }} {% endif %}</i></p>
            <br>
          </div>
        {% endif %}
      {% endif %}
    {% endfor %}
  </div>
  <div class="column">
    {% for people in site.data.alumni %}
      {% if people.role == "MS" %}
        {% if people.col == 2 %}
          <div class="row">
                {% if people.website %}
                  <p><a href="{{ people.website }}">{{ people.name }}</a></p>
                {% else %}
                  <p>{{ people.name }}</p>
                {% endif %}
            <p><i> Class of {{ people.year }}{% if people.now %}, {{ people.now }} {% endif %}</i></p>
            <br>
          </div>
        {% endif %}
      {% endif %}
    {% endfor %}
  </div>
</div>

<div class="row">
  <h4>Undergraduate</h4>
  <div class="column">
    {% for people in site.data.alumni %}
      {% if people.role == "BS" %}
        {% if people.col == 1 %}
          <div class="row">
                {% if people.website %}
                  <p><a href="{{ people.website }}">{{ people.name }}</a></p>
                {% else %}
                  <p>{{ people.name }}</p>
                {% endif %}
            <p><i> Class of {{ people.year }}{% if people.now %}, {{ people.now }} {% endif %}</i></p>
            <br>
          </div>
        {% endif %}
      {% endif %}
    {% endfor %}
  </div>
  <div class="column">
    {% for people in site.data.alumni %}
      {% if people.role == "BS" %}
        {% if people.col == 2 %}
          <div class="row">
                {% if people.website %}
                  <p><a href="{{ people.website }}">{{ people.name }}</a></p>
                {% else %}
                  <p>{{ people.name }}</p>
                {% endif %}
            <p><i> Class of {{ people.year }}{% if people.now %}, {{ people.now }} {% endif %}</i></p>
            <br>
          </div>
        {% endif %}
      {% endif %}
    {% endfor %}
  </div>
</div>

<div class="row">
  <h4>International Summer Interns</h4>
  <div class="column">
    {% for people in site.data.alumni %}
      {% if people.role == "Intern" %}
        {% if people.col == 1 %}
          <div class="row">
                {% if people.website %}
                  <p><a href="{{ people.website }}">{{ people.name }}</a></p>
                {% else %}
                  <p>{{ people.name }}</p>
                {% endif %}
            <p><i> Class of {{ people.year }}{% if people.now %}, {{ people.now }} {% endif %}</i></p>
            <br>
          </div>
        {% endif %}
      {% endif %}
    {% endfor %}
  </div>
  <div class="column">
    {% for people in site.data.alumni %}
      {% if people.role == "Intern" %}
        {% if people.col == 2 %}
          <div class="row">
                {% if people.website %}
                  <p><a href="{{ people.website }}">{{ people.name }}</a></p>
                {% else %}
                  <p>{{ people.name }}</p>
                {% endif %}
            <p><i> Class of {{ people.year }}{% if people.now %}, {{ people.now }} {% endif %}</i></p>
            <br>
          </div>
        {% endif %}
      {% endif %}
    {% endfor %}
  </div>
</div>
