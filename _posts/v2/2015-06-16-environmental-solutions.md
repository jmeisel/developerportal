---
published: true
permalink: "/environmental_solutions.html"
title: Environmental Solutions Toolkit
layout: body
---

#Environmental Solutions Toolkit

{% include environmental-solutions-tabs %}

##Resource URL

This endpoint will search environmental solutions with the defined languages: english, chinese, french, portuguese, and spanish.

{% include environmental-solutions-query.html %}

##Search Parameters for Environmental Solutions Toolkit

###keyword

Returns solutions for a match in the **name_chinese**, **name_english**, **name_french**, **name_portuguese**, or **name_spanish** fields.

    {{ site.webservices_baseurl }}/v2/environmental_solutions/search?api_key={your key}&q={keyword}

**_Example_**


###size + offset

The **size** parameter allows you to configure the number of results to be returned up to a maximum of 100. The **offset** parameter defines the offset from the first result you want to fetch. Unless specified the API returns 10 results at a time.

**_Example_**


###Return Values

| Field           | Description                                                     |
| --------------- | --------------------------------------------------------------- |
| name_chinese
| name_english
| name_french
| name_portuguese
| name_spanish
| source_created_at
| source_updated_at
| source_id
