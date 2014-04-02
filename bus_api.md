---
title: BUS API
---

# Comments

* TOC
{:toc}

## ROUTING

    GET /getroute.php
    
    
### Parameters

Name | Type | Description 
-----|------|--------------
`changeMargin`|`integer` | **Required**. Foo
`walkSpeed`|`integer` | **Required**. Foo
`maxTotWalkDist`|`string` | **Required**. Foo
`timeDirection`|`string` | **Required**. Foo
`numberRoutes`|`integer` | **Required**. Foo
`timestamp`|`time` | **Required**. Foo
`start[x]`|`integer` | **Required**. Foo
`start[y]`|`integer` | **Required**. Foo
`end[x]`|`integer` | **Required**. Foo
`end[y]`|`integer` | **Required**. Foo
`via`|`time` | **Required**. Foo
`excludedLines`|`time` | **Required**. Foo
`includedLines`|`time` | **Required**. Foo
`token`|`string` | **Required**. Foo

### Response

<%= headers 200 %>
<%= json(:gist_comment) { |h| [h] } %>

## Geocoding

    GET /geocode.php

### Response

<%= headers 200 %>
<%= json :gist_comment %>


    application/vnd.github.VERSION.raw+json
    application/vnd.github.VERSION.text+json
    application/vnd.github.VERSION.html+json
    application/vnd.github.VERSION.full+json
