{% if site.style == 'dark' %}
  {% assign icon_color = "#ffffff" %}
{% else %}
  {% assign icon_color = "#24292e" %}
{% endif %}

{% assign posts_total = site.posts | size %}

{% assign user = site.github.owner %}

{% if page.path contains '_posts' %}
  {% assign page_title = page.title %}
  {% assign meta_description = page.content | strip_html | strip_newlines | xml_escape | truncate: 300 %}
{% else %}
  {% assign page_title = user.name %}
  {% assign meta_description = user.bio | strip_html | strip_newlines | xml_escape | truncate: 300 %}
{% endif %}

<!doctype html>
<html class="min-height-full" data-theme="light">
  <head>
    {% include google-analytics.html %}
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <link rel="stylesheet" href="/assets/site.css">
    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/turbolinks/5.2.0/turbolinks.js"></script>
    <meta charset="utf-8">
    <title>Carlos Gamino</title>
    <meta name="description" content="{{ meta_description }}" />
    <meta property="og:title" content="Carlos Gamino" />
    <meta property="og:image" content="{{ site.profPic }}"/>
    <meta property="og:description" content="{{ meta_description }}" />
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  </head>
  <div class="wrapper">
  <body class="min-height-full">
    {% include navigation.html %}
    <main class="site-content">