---
layout: page
title: Contact
permalink: /contact
comments: false
author: pur
---

{% assign author = site.authors[page.author] %}
<div class="d-flex authorbox align-items-center">
    <div class="col-xl-2 mr-4 text-center">
        {% if author.avatar %}
        <img class="author-contact" src="{{site.baseurl}}/{{ author.avatar }}" alt="{{ author.display_name }}">
        {% else %}
        <img class="author-contact" src="https://www.gravatar.com/avatar/{{ author.gravatar }}?s=250&d=mm&r=x" alt="{{ author.display_name }}">
        {% endif %}
    </div>
    <div class="col-md-10"> 
        <a target="_blank" class="text-dark h4">About {{ author.display_name }}</a>   
        <a target="_blank" href="{{ author.twitter }}" class="btn-sm"><i class="fab fa-twitter"></i></a>        
        <a target="_blank" href="{{ author.linkedin }}" class="btn-sm"><i class="fab fa-linkedin"></i></a>        
        <a target="_blank" href="{{ author.ihub }}" class="btn-sm"><i class="fab fa-github-alt"></i></a>        
        <span class="author-description d-block mt-2">{{ author.description }}</span>            
    </div>
</div>

<form action="{{site.formspring-enpoint}}" method="POST">    
    <p class="mb-4">Please send your message to {{site.name}}. We will reply as soon as possible!</p>
        <div class="form-group row">
            <div class="col-md-6">
                <input class="form-control" type="text" name="name" placeholder="Name*" required>
            </div>
            <div class="col-md-6">
                <input class="form-control" type="email" name="_replyto" placeholder="E-mail Address*" required>
            </div>
        </div>
    <textarea rows="8" class="form-control mb-3" name="message" placeholder="Message*" required></textarea>    
    <input class="btn btn-dark" type="submit" value="Send">
</form>