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
`changeMargin`|`integer` | The minimum number of minutes between changes. Default 3, range 0-10.
`walkSpeed`|`integer` | Walking speed, Optional, default 70 m/min, range 1-500.
`maxTotWalkDist`|`string` | **Required**. Foo
`timeDirection`|`string` | **Required**. Foo
`numberRoutes`|`integer` | **Required**. Foo
`timestamp`|`time` | **Required**. Foo
`start[x]`|`integer` | Coordinate
`start[y]`|`integer` | Coordinate
`end[x]`|`integer` | Coordinate
`end[y]`|`integer` | Coordinate
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
