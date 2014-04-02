Turku Bus API
======

(Unofficial) guide to Turku BUS API

## Get routes

    GET /getroute.php
    
    
### Parameters

Name | Type | Description 
-----|------|--------------
`request[changeMargin]`|`integer` | The minimum number of minutes between changes. Default 3, range 0-10.
`request[walkSpeed]`|`integer` | Walking speed, Optional, default 70 m/min, range 1-500.
`request[maxTotWalkDist]`|`string` | Maximum walking distance. no_restriction or range 500-10000.
`request[timeDirection]`|`string` |  backward or forward
`request[numberRoutes]`|`integer` | Maximum number of routes. Default 5.
`request[routingMethod]`|`integer` | Routing method. default, minchanges, fastest, minwalk
`request[timestamp]`|`time` | Departure time
`request[start][x]`|`float` | Coordinate
`request[start][y]`|`float` | Coordinate
`request[end][x]`|`float` | Coordinate
`request[end][y]`|`float` | Coordinate
`request[via]`|`float` | Coordinate
`request[excludedLines]`|`string` | Lines names to be excluded, see lines
`request[includedLines]`|`string` | Lines names to be included, see lines
`request[token]`|`string` | **Required**. API Token

### Response
```xml

<MTRXML version="1.0">
        <ROUTE from="start" to="end">
                <LENGTH time="0.024" dist="1.689"/>
                <POINT uid="start" x="3240112.5" y="6713845.5">
                        <ARRIVAL date="20140402" time="1152"/>
                        <DEPARTURE date="20140402" time="1153"/>
                </POINT>
                <WALK>
                        <LENGTH time="0.024" dist="1.689"/>
                        <POINT uid="start" x="3240112.5" y="6713845.5">
                                <ARRIVAL date="20140402" time="1152"/>
                                <DEPARTURE date="20140402" time="1153"/>
                        </POINT>
                        <SHAPE time="0" dist="1.689">
3240111.8 6713845.1 `` 0
3240111.8 6713845.1 `` 0
                        </SHAPE>
                        <POINT uid="end" x="3240112.5" y="6713845.5">
                                <ARRIVAL date="20140402" time="1152"/>
                                <DEPARTURE date="20140402" time="1153"/>
                        </POINT>
                </WALK>
                <POINT uid="end" x="3240112.5" y="6713845.5">
                        <ARRIVAL date="20140402" time="1152"/>
                        <DEPARTURE date="20140402" time="1153"/>
                </POINT>
        </ROUTE>
</MTRXML>

```

### Lines
List of available lines;Askainen, Granvik, Helsinki, Hirvikoski, Houtskari, Huittinen, Karjala, Kemiö, Kittuis/Galtby, Korppoo, Koski TL, Kustavi, Kyrö, Laajoki, Lemu th, Lielahti, Livonsaari, Loimaa, Masku, Miiainen, Mossala, Mynämäki, Nousiainen, Ohensaari, Oripää, P1, P2, P3, Paimio, Paimio motelli, Palv., Parainen, Rantola, Rauma, Salo, Sauvo, Sauvo th, Sydmo, Taalintehdas, Tampere, Teersalo, Turku, Uusikaupunki, Valpperi, tien/Kustavintien risteys, 1, 01, 2, 2A, 3, 4, 6, 8, 9, 11, 11A, 12, 13, 14, 15, 18, 20, 21, 22, 23, 28, 30, 31, 32, 33, 34, 36, 40, 42, 50, 51, 52, 53, 54, 55, 56, 58, 61, 66, 67, 72, 73, 74, 80, 83, 88, 90, 91, 99, 100, 109, 110, 111, 112, 115, 116, 118, 119, 191, 192, 194, 195, 201, 211, 212, 213, 221, 222, 223, 224, 231, 232, 280, 282, 285, 320, 321, 420, 422, 429

## Geocoding

    GET /geocode.php

### Response
```json
{
  "key": "Varusmestarintie, Turku",
  "data": {
    "locations": [
      {
        "category": "street",
        "x":"3240138.000000",
        "y":"6718301.500000",
        "name":"Varusmestarintie",
        "city":"Turku"
      }
    ]
  },
  "status": 0
}
```
