---
permalink: "/ita-taxonomies.html"
layout: body
title: ITA Taxonomies
published: true
---

#ITA Taxonomies API

{% include taxonomies-tabs %}

##Resource URL

{% include taxonomies-query.html %}

##Search Parameters for ITA Taxonomies

###keyword

Returns taxonomy terms for a match within the **name** and **parent_names** fields.

    {{ site.webservices_baseurl }}/v2/ita_taxonomies/search?api_key={your key}&q={keyword}

**_Example_**

{% include taxonomies-query-keyword.html %}

###taxonomies

Returns taxonomy terms that are members of the specified taxonomies.  Enter muliple values separated by commas.

    {{ site.webservices_baseurl }}/v2/ita_taxonomies/search?api_key={your key}&taxonomies={value1,value2}

**_Example_**

{% include taxonomies-query-taxonomies.html %}

###size + offset

The **size** parameter allows you to configure the number of results to be returned up to a maximum of 100. The **offset** parameter defines the offset from the first result you want to fetch. Unless specified the API returns 10 results at a time.

**_Example_**

{% include taxonomies-query-size.html %}

##Last Updated and Last Imported

Recency information about each source queried is given in **sources_used** in the following fields:

| Field	| Description |
| ------| -------------|
| source | The name of the issuing agency. |
| source_last_updated | The most recent date and time the data changed. |
| last_imported | The most recent date and time the data was imported. |

The *source_last_updated* field reflects the most recent date and time we noticed that the issuing agency had updated the data. We check for updates and import lists at the same time daily.

###Return Values

| Field             | Description                                                     |
| ----------------- | --------------------------------------------------------------- |
| id         		| The id assigned to the term.                                    |
| name              | The name of the given taxonomy term.                            |
| taxonomy          | The taxonomy under which the given term belongs.                |
| parent_names      | The names of any parent terms, if any, for the given term.      |

