---
title: Archive
description: "All of the posts in Derek’s Digital Garden"
og-type: website
permalink: /archive
nav: custom
custom-nav: 
    - '<a href="/blog/tags" title="Tags">Tags</a>&nbsp;|&nbsp;'
    - '<a style="cursor: pointer;" onclick="toggleSearchBar()" title="Search" >Search</a>&nbsp;|&nbsp;'
    - '<a href="/blog/random" title="Random post">Random</a>'
---

<div id="search-bar">
{%- include search.html -%}
</div>

<h2 id="tags">Tags</h2>

{% assign sortedTags = site.tags | sort %}

<div class="tag-list">
{% for tag in sortedTags %}
    <a href="#{{tag[0]}}">{{ tag[0] }}&nbsp;({{ tag[1] | size }})</a>
{% endfor %}
</div>

<h2>Archive Posts</h2>

{% for post in site.posts %}
{%- unless post.categories contains "rss-club" or 
post.categories contains "now"-%}
{% include blog-listing.html %}
{% endunless %}
{% endfor %}


<!-- this makes the search bar display a bit nicer but can easily be removed -->

<script>

let searchBarStatus = sessionStorage.getItem("searchBarStatus");

if (!searchBarStatus) {
    sessionStorage.setItem("searchBarStatus", "False");
    }
    else if (searchBarStatus === "True") {
    document.getElementById("search-bar").setAttribute("style", "display: block");
    }

function toggleSearchBar() {
    
    let searchBarStatus = sessionStorage.getItem("searchBarStatus");

    if (searchBarStatus === "False") {
        document.getElementById("search-bar").setAttribute("style", "display: block");
        sessionStorage.setItem("searchBarStatus", "True");
    } else if (searchBarStatus === "True") {
        document.getElementById("search-bar").setAttribute("style", "display: none");
        sessionStorage.setItem("searchBarStatus", "False");
    }    
}

</script>