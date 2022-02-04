---
layout: post
title: Components
permalink: /components/
content-type: eg
---

{% if jekyll.environment == "production" %}

    {% comment %}
        # When running in production, `bookshop-hosted` in package.json
        # builds a static hosted version of your component browser
        # to the following path.
    {% endcomment %}
    {% bookshop_browser /assets/bookshop-hosted.js %}

{% else %}

    {% comment %}
        # When running locally, `bookshop-dev` in package.json
        # hosts a local webserver that powers your component browser
        # and enables hot-reloading withing the component browser.
    {% endcomment %}
    {% bookshop_browser :6061 %}

{% endif %}
