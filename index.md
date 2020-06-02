---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: page
title: AS207960
---

<main role="main" class="flex-shrink-0">
  <div class="container">
    <div class="row">
      <div class="col-md-8">
        <div class="jumbotron">
          <div class="row">
            <div class="col-md-4">
              <img src="{{site.logo}}" class="mw-100" />
            </div>
            <div class="col-md-8">
              <h1 class="display-4">{{site.title}}</h1>
              <p class="lead">{{site.tagline}}</p>
              <p>{{ site.description }}</p>
              {% for button in site.buttons %}
              <a class="btn btn-primary btn-lg" href="{{ button.url }}" role="button">{{ button.title }}</a>
              {% endfor %}
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card content-section">
          <div class="card-body">
            <h3>Latest Posts</h3>
            {% if site.posts %}
              <ul class="list-group">
                {% for post in site.posts limit:3 %}
                <li class="list-group-item">
                  <a href="{{ post.url }}">
                    <h3>{{ post.title }}</h3>
                  </a>
                  <p class="blogdate">{{ post.date | date: "%d %B %Y" }}</p>
                  <div>{{ post.content | truncatehtml | truncatewords: 60 }}</div>
                </li>
                {% endfor %}
            {% else %}
            <h4>No posts, Watch this space</h4>    
            {% endif %}
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-md-6">
        <h1>Who runs AS207960?</h1>
        <h3><a href="https://magicalcodewit.ch/">Q</a></h3>
        <h3><a href="https://lordbonzi.pro">Alfie Foster</a></h3>
        <h3><a href="https://eater.me">eater</a></h3>
      </div>
      <div class="col-md-6">
        <h1>Peering</h1>
        <h3>We have an open policy; if you can get a link to us, you can peer</h3>
        <h3>See our <a href="https://www.peeringdb.com/net/21249">PeeringDB</a> entry for more info</h3>
      </div>
    </div>
    <div class="row align-items-center">
      <div class="col-sm text-center my-3">
        <img class="mw-100" src="/assets/img/MANRS_RGB_vertical_logo_dark.jpg" alt="MANRS Member" />
      </div>
      <div class="col-sm text-center my-3">
        <img class="mw-100" src="/assets/img/acc_reg_cnic.png" alt="CentralNIC accredited registrar" />
      </div>
      <div class="col-sm text-center my-3">
        <img class="mw-100" src="/assets/img/Nominet_ACP_Land_RGB_Light_Blue.png"
          alt="Nominet Accredited Channel Partner" />
      </div>
      <div class="col-sm text-center my-3">
        <a href="https://www.nominet.uk/go/terms"><img class="mw-100"
            src="/assets/img/Nominet_Terms_Online_RGB_Teal.png" alt="Nominet T&Cs" /></a>
      </div>
    </div>
  </div>
</main>
