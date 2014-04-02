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
`maxTotWalkDist`|`string` | no_restriction or r ange 500-10000.
`timeDirection`|`string` |  backward or forward
`numberRoutes`|`integer` | Maximum number of routes. Default 5, range??
`routingMethod`|`integer` | Routing method. default, minchanges, fastest, minwalk
`timestamp`|`time` | Departure time
`start[x]`|`integer` | Coordinate
`start[y]`|`integer` | Coordinate
`end[x]`|`integer` | Coordinate
`end[y]`|`integer` | Coordinate
`via`|`integer` | Coordinate
`excludedLines`|`string` | Lines names to be excluded, see lines
`includedLines`|`string` | Lines names to be included, see lines
`token`|`string` | **Required**. API Token

### Response
```xml

<MTRXML version="1.0">
	<ROUTE from="start" to="end">
		<LENGTH time="14.199" dist="5397.238"/>
		<POINT uid="start" x="3239920.8" y="6714163.5">
			<ARRIVAL date="20140402" time="1152"/>
			<DEPARTURE date="20140402" time="1153"/>
		</POINT>
		<WALK>
			<LENGTH time="1.090" dist="88.535"/>
			<POINT uid="start" x="3239920.8" y="6714163.5">
				<ARRIVAL date="20140402" time="1152"/>
				<DEPARTURE date="20140402" time="1153"/>
			</POINT>
			<SHAPE time="0" dist="29.258">
3239920.0 6714163.0 `` 0
3239905.3 6714187.3 `` 0
			</SHAPE>
			<MAPLOC x="3239905.3" y="6714187.3" type="12131">
				<ARRIVAL date="20140402" time="1153"/>
				<DEPARTURE date="20140402" time="1154"/>
				<NAME lang="1" val="Maariankatu"/>
			</MAPLOC>
			<SHAPE time="1" dist="59.277">
3239905.3 6714187.3 `` 0
3239864.2 6714162.7 `` 0
			</SHAPE>
			<STOP code="2:472" x="3239870.0" y="6714153.0" id="1229">
				<ARRIVAL date="20140402" time="1154"/>
				<DEPARTURE date="20140402" time="1154"/>
				<NAME lang="1" val="Puutori"/>
				<NAME lang="2" val="Cygnaeus skola"/>
				<XTRA name="digistop_id" val="472"/>
			</STOP>
		</WALK>
		<LINE id="1013" code="18" type="1" mobility="0">
			<LENGTH time="13.000" dist="5297.209"/>
			<STOP code="2:472" x="3239870.0" y="6714153.0" id="1229" ord="27">
				<ARRIVAL date="20140402" time="1154"/>
				<DEPARTURE date="20140402" time="1154"/>
				<NAME lang="1" val="Puutori"/>
				<NAME lang="2" val="Cygnaeus skola"/>
				<XTRA name="digistop_id" val="472"/>
			</STOP>
			<SHAPE time="1" dist="349.860">
3239870.0 6714153.0 `` 0
3239989.0 6714482.0 `` 0
			</SHAPE>
			<STOP code="2:19" x="3239989.0" y="6714482.0" id="845">
				<ARRIVAL date="20140402" time="1155"/>
				<DEPARTURE date="20140402" time="1155"/>
				<NAME lang="1" val="Linja-autoasema"/>
				<NAME lang="2" val="Linjebilstationen"/>
				<XTRA name="digistop_id" val="19"/>
			</STOP>
			<SHAPE time="1" dist="449.694">
3239989.0 6714482.0 `` 0
3239950.0 6714930.0 `` 0
			</SHAPE>
			<STOP code="2:174" x="3239950.0" y="6714930.0" id="729">
				<ARRIVAL date="20140402" time="1156"/>
				<DEPARTURE date="20140402" time="1156"/>
				<NAME lang="1" val="Autistenaukio"/>
				<NAME lang="2" val="Autisplan"/>
				<XTRA name="digistop_id" val="174"/>
			</STOP>
			<SHAPE time="1" dist="186.657">
3239950.0 6714930.0 `` 0
3240054.0 6715085.0 `` 0
			</SHAPE>
			<STOP code="2:175" x="3240054.0" y="6715085.0" id="740">
				<ARRIVAL date="20140402" time="1157"/>
				<DEPARTURE date="20140402" time="1157"/>
				<NAME lang="1" val="Oskarinkuja"/>
				<NAME lang="2" val="Oskarsgränd"/>
				<XTRA name="digistop_id" val="175"/>
			</STOP>
			<SHAPE time="0" dist="287.127">
3240054.0 6715085.0 `` 0
3240113.0 6715366.0 `` 0
			</SHAPE>
			<STOP code="2:612" x="3240113.0" y="6715366.0" id="1390">
				<ARRIVAL date="20140402" time="1157"/>
				<DEPARTURE date="20140402" time="1157"/>
				<NAME lang="1" val="Kastuntie"/>
				<NAME lang="2" val="Kastuvägen"/>
				<XTRA name="digistop_id" val="612"/>
			</STOP>
			<SHAPE time="1" dist="463.341">
3240113.0 6715366.0 `` 0
3239974.0 6715808.0 `` 0
			</SHAPE>
			<STOP code="2:613" x="3239974.0" y="6715808.0" id="1391">
				<ARRIVAL date="20140402" time="1158"/>
				<DEPARTURE date="20140402" time="1158"/>
				<NAME lang="1" val="Parrantie"/>
				<NAME lang="2" val="Partavägen"/>
				<XTRA name="digistop_id" val="613"/>
			</STOP>
			<SHAPE time="2" dist="768.500">
3239974.0 6715808.0 `` 0
3240022.0 6716575.0 `` 0
			</SHAPE>
			<STOP code="2:979" x="3240022.0" y="6716575.0" id="1741">
				<ARRIVAL date="20140402" time="1200"/>
				<DEPARTURE date="20140402" time="1200"/>
				<NAME lang="1" val="Markulanpuisto"/>
				<NAME lang="2" val="Markulaparken"/>
				<XTRA name="digistop_id" val="979"/>
			</STOP>
			<SHAPE time="0" dist="296.061">
3240022.0 6716575.0 `` 0
3240156.0 6716839.0 `` 0
			</SHAPE>
			<STOP code="2:980" x="3240156.0" y="6716839.0" id="1743">
				<ARRIVAL date="20140402" time="1200"/>
				<DEPARTURE date="20140402" time="1200"/>
				<NAME lang="1" val="Toukolanpuistikko"/>
				<NAME lang="2" val="Toukolaskvären"/>
				<XTRA name="digistop_id" val="980"/>
			</STOP>
			<SHAPE time="1" dist="621.007">
3240156.0 6716839.0 `` 0
3240327.0 6717436.0 `` 0
			</SHAPE>
			<STOP code="2:981" x="3240327.0" y="6717436.0" id="1744">
				<ARRIVAL date="20140402" time="1201"/>
				<DEPARTURE date="20140402" time="1201"/>
				<NAME lang="1" val="Palli"/>
				<NAME lang="2" val="Palli"/>
				<XTRA name="digistop_id" val="981"/>
			</STOP>
			<SHAPE time="1" dist="385.251">
3240327.0 6717436.0 `` 0
3240070.0 6717723.0 `` 0
			</SHAPE>
			<STOP code="2:982" x="3240070.0" y="6717723.0" id="1745">
				<ARRIVAL date="20140402" time="1202"/>
				<DEPARTURE date="20140402" time="1202"/>
				<NAME lang="1" val="Runosmäen terveysasema"/>
				<NAME lang="2" val="Runosmäen terveysasema"/>
				<XTRA name="digistop_id" val="982"/>
			</STOP>
			<SHAPE time="1" dist="342.286">
3240070.0 6717723.0 `` 0
3239732.0 6717777.0 `` 0
			</SHAPE>
			<STOP code="2:984" x="3239732.0" y="6717777.0" id="1747">
				<ARRIVAL date="20140402" time="1203"/>
				<DEPARTURE date="20140402" time="1203"/>
				<NAME lang="1" val="Signalistinpolku"/>
				<NAME lang="2" val="Signaliststigen"/>
				<XTRA name="digistop_id" val="984"/>
			</STOP>
			<SHAPE time="1" dist="233.225">
3239732.0 6717777.0 `` 0
3239637.0 6717990.0 `` 0
			</SHAPE>
			<STOP code="2:985" x="3239637.0" y="6717990.0" id="1748">
				<ARRIVAL date="20140402" time="1204"/>
				<DEPARTURE date="20140402" time="1204"/>
				<NAME lang="1" val="Munterinkatu"/>
				<NAME lang="2" val="Muntersgatan"/>
				<XTRA name="digistop_id" val="985"/>
			</STOP>
			<SHAPE time="0" dist="241.661">
3239637.0 6717990.0 `` 0
3239537.0 6718210.0 `` 0
			</SHAPE>
			<STOP code="2:986" x="3239537.0" y="6718210.0" id="1749">
				<ARRIVAL date="20140402" time="1204"/>
				<DEPARTURE date="20140402" time="1204"/>
				<NAME lang="1" val="Nostoväenkatu"/>
				<NAME lang="2" val="Lantvärnsgatan"/>
				<XTRA name="digistop_id" val="986"/>
			</STOP>
			<SHAPE time="1" dist="406.710">
3239537.0 6718210.0 `` 0
3239895.0 6718403.0 `` 0
			</SHAPE>
			<STOP code="2:1013" x="3239895.0" y="6718403.0" id="16">
				<ARRIVAL date="20140402" time="1205"/>
				<DEPARTURE date="20140402" time="1205"/>
				<NAME lang="1" val="Parolanpuisto"/>
				<NAME lang="2" val="Parolaparken"/>
				<XTRA name="digistop_id" val="1013"/>
			</STOP>
			<SHAPE time="2" dist="265.827">
3239895.0 6718403.0 `` 0
3240137.0 6718293.0 `` 0
			</SHAPE>
			<STOP code="2:1014" x="3240137.0" y="6718293.0" id="17" ord="41">
				<ARRIVAL date="20140402" time="1207"/>
				<DEPARTURE date="20140402" time="1207"/>
				<NAME lang="1" val="Kiikku"/>
				<NAME lang="2" val="Kiikku"/>
				<XTRA name="digistop_id" val="1014"/>
			</STOP>
		</LINE>
		<WALK>
			<LENGTH time="0.109" dist="11.494"/>
			<STOP code="2:1014" x="3240137.0" y="6718293.0" id="17">
				<ARRIVAL date="20140402" time="1207"/>
				<DEPARTURE date="20140402" time="1207"/>
				<NAME lang="1" val="Kiikku"/>
				<NAME lang="2" val="Kiikku"/>
				<XTRA name="digistop_id" val="1014"/>
			</STOP>
			<SHAPE time="0" dist="11.494">
3240139.7 6718294.0 `` 0
3240137.0 6718301.2 `` 0
			</SHAPE>
			<POINT uid="end" x="3240138.0" y="6718301.5">
				<ARRIVAL date="20140402" time="1207"/>
				<DEPARTURE date="20140402" time="1208"/>
			</POINT>
		</WALK>
		<POINT uid="end" x="3240138.0" y="6718301.5">
			<ARRIVAL date="20140402" time="1207"/>
			<DEPARTURE date="20140402" time="1208"/>
		</POINT>
	</ROUTE>
	<ROUTE from="start" to="end">
		<LENGTH time="14.199" dist="5397.238"/>
		<POINT uid="start" x="3239920.8" y="6714163.5">
			<ARRIVAL date="20140402" time="1159"/>
			<DEPARTURE date="20140402" time="1200"/>
		</POINT>
		<WALK>
			<LENGTH time="1.090" dist="88.535"/>
			<POINT uid="start" x="3239920.8" y="6714163.5">
				<ARRIVAL date="20140402" time="1159"/>
				<DEPARTURE date="20140402" time="1200"/>
			</POINT>
			<SHAPE time="0" dist="29.258">
3239920.0 6714163.0 `` 0
3239905.3 6714187.3 `` 0
			</SHAPE>
			<MAPLOC x="3239905.3" y="6714187.3" type="12131">
				<ARRIVAL date="20140402" time="1200"/>
				<DEPARTURE date="20140402" time="1201"/>
				<NAME lang="1" val="Maariankatu"/>
			</MAPLOC>
			<SHAPE time="1" dist="59.277">
3239905.3 6714187.3 `` 0
3239864.2 6714162.7 `` 0
			</SHAPE>
			<STOP code="2:472" x="3239870.0" y="6714153.0" id="1229">
				<ARRIVAL date="20140402" time="1201"/>
				<DEPARTURE date="20140402" time="1201"/>
				<NAME lang="1" val="Puutori"/>
				<NAME lang="2" val="Cygnaeus skola"/>
				<XTRA name="digistop_id" val="472"/>
			</STOP>
		</WALK>
		<LINE id="1027" code="18" type="1" mobility="0">
			<LENGTH time="13.000" dist="5297.209"/>
			<STOP code="2:472" x="3239870.0" y="6714153.0" id="1229" ord="27">
				<ARRIVAL date="20140402" time="1201"/>
				<DEPARTURE date="20140402" time="1201"/>
				<NAME lang="1" val="Puutori"/>
				<NAME lang="2" val="Cygnaeus skola"/>
				<XTRA name="digistop_id" val="472"/>
			</STOP>
			<SHAPE time="1" dist="349.860">
3239870.0 6714153.0 `` 0
3239989.0 6714482.0 `` 0
			</SHAPE>
			<STOP code="2:19" x="3239989.0" y="6714482.0" id="845">
				<ARRIVAL date="20140402" time="1202"/>
				<DEPARTURE date="20140402" time="1202"/>
				<NAME lang="1" val="Linja-autoasema"/>
				<NAME lang="2" val="Linjebilstationen"/>
				<XTRA name="digistop_id" val="19"/>
			</STOP>
			<SHAPE time="1" dist="449.694">
3239989.0 6714482.0 `` 0
3239950.0 6714930.0 `` 0
			</SHAPE>
			<STOP code="2:174" x="3239950.0" y="6714930.0" id="729">
				<ARRIVAL date="20140402" time="1203"/>
				<DEPARTURE date="20140402" time="1203"/>
				<NAME lang="1" val="Autistenaukio"/>
				<NAME lang="2" val="Autisplan"/>
				<XTRA name="digistop_id" val="174"/>
			</STOP>
			<SHAPE time="1" dist="186.657">
3239950.0 6714930.0 `` 0
3240054.0 6715085.0 `` 0
			</SHAPE>
			<STOP code="2:175" x="3240054.0" y="6715085.0" id="740">
				<ARRIVAL date="20140402" time="1204"/>
				<DEPARTURE date="20140402" time="1204"/>
				<NAME lang="1" val="Oskarinkuja"/>
				<NAME lang="2" val="Oskarsgränd"/>
				<XTRA name="digistop_id" val="175"/>
			</STOP>
			<SHAPE time="0" dist="287.127">
3240054.0 6715085.0 `` 0
3240113.0 6715366.0 `` 0
			</SHAPE>
			<STOP code="2:612" x="3240113.0" y="6715366.0" id="1390">
				<ARRIVAL date="20140402" time="1204"/>
				<DEPARTURE date="20140402" time="1204"/>
				<NAME lang="1" val="Kastuntie"/>
				<NAME lang="2" val="Kastuvägen"/>
				<XTRA name="digistop_id" val="612"/>
			</STOP>
			<SHAPE time="1" dist="463.341">
3240113.0 6715366.0 `` 0
3239974.0 6715808.0 `` 0
			</SHAPE>
			<STOP code="2:613" x="3239974.0" y="6715808.0" id="1391">
				<ARRIVAL date="20140402" time="1205"/>
				<DEPARTURE date="20140402" time="1205"/>
				<NAME lang="1" val="Parrantie"/>
				<NAME lang="2" val="Partavägen"/>
				<XTRA name="digistop_id" val="613"/>
			</STOP>
			<SHAPE time="2" dist="768.500">
3239974.0 6715808.0 `` 0
3240022.0 6716575.0 `` 0
			</SHAPE>
			<STOP code="2:979" x="3240022.0" y="6716575.0" id="1741">
				<ARRIVAL date="20140402" time="1207"/>
				<DEPARTURE date="20140402" time="1207"/>
				<NAME lang="1" val="Markulanpuisto"/>
				<NAME lang="2" val="Markulaparken"/>
				<XTRA name="digistop_id" val="979"/>
			</STOP>
			<SHAPE time="0" dist="296.061">
3240022.0 6716575.0 `` 0
3240156.0 6716839.0 `` 0
			</SHAPE>
			<STOP code="2:980" x="3240156.0" y="6716839.0" id="1743">
				<ARRIVAL date="20140402" time="1207"/>
				<DEPARTURE date="20140402" time="1207"/>
				<NAME lang="1" val="Toukolanpuistikko"/>
				<NAME lang="2" val="Toukolaskvären"/>
				<XTRA name="digistop_id" val="980"/>
			</STOP>
			<SHAPE time="1" dist="621.007">
3240156.0 6716839.0 `` 0
3240327.0 6717436.0 `` 0
			</SHAPE>
			<STOP code="2:981" x="3240327.0" y="6717436.0" id="1744">
				<ARRIVAL date="20140402" time="1208"/>
				<DEPARTURE date="20140402" time="1208"/>
				<NAME lang="1" val="Palli"/>
				<NAME lang="2" val="Palli"/>
				<XTRA name="digistop_id" val="981"/>
			</STOP>
			<SHAPE time="1" dist="385.251">
3240327.0 6717436.0 `` 0
3240070.0 6717723.0 `` 0
			</SHAPE>
			<STOP code="2:982" x="3240070.0" y="6717723.0" id="1745">
				<ARRIVAL date="20140402" time="1209"/>
				<DEPARTURE date="20140402" time="1209"/>
				<NAME lang="1" val="Runosmäen terveysasema"/>
				<NAME lang="2" val="Runosmäen terveysasema"/>
				<XTRA name="digistop_id" val="982"/>
			</STOP>
			<SHAPE time="1" dist="342.286">
3240070.0 6717723.0 `` 0
3239732.0 6717777.0 `` 0
			</SHAPE>
			<STOP code="2:984" x="3239732.0" y="6717777.0" id="1747">
				<ARRIVAL date="20140402" time="1210"/>
				<DEPARTURE date="20140402" time="1210"/>
				<NAME lang="1" val="Signalistinpolku"/>
				<NAME lang="2" val="Signaliststigen"/>
				<XTRA name="digistop_id" val="984"/>
			</STOP>
			<SHAPE time="1" dist="233.225">
3239732.0 6717777.0 `` 0
3239637.0 6717990.0 `` 0
			</SHAPE>
			<STOP code="2:985" x="3239637.0" y="6717990.0" id="1748">
				<ARRIVAL date="20140402" time="1211"/>
				<DEPARTURE date="20140402" time="1211"/>
				<NAME lang="1" val="Munterinkatu"/>
				<NAME lang="2" val="Muntersgatan"/>
				<XTRA name="digistop_id" val="985"/>
			</STOP>
			<SHAPE time="0" dist="241.661">
3239637.0 6717990.0 `` 0
3239537.0 6718210.0 `` 0
			</SHAPE>
			<STOP code="2:986" x="3239537.0" y="6718210.0" id="1749">
				<ARRIVAL date="20140402" time="1211"/>
				<DEPARTURE date="20140402" time="1211"/>
				<NAME lang="1" val="Nostoväenkatu"/>
				<NAME lang="2" val="Lantvärnsgatan"/>
				<XTRA name="digistop_id" val="986"/>
			</STOP>
			<SHAPE time="1" dist="406.710">
3239537.0 6718210.0 `` 0
3239895.0 6718403.0 `` 0
			</SHAPE>
			<STOP code="2:1013" x="3239895.0" y="6718403.0" id="16">
				<ARRIVAL date="20140402" time="1212"/>
				<DEPARTURE date="20140402" time="1212"/>
				<NAME lang="1" val="Parolanpuisto"/>
				<NAME lang="2" val="Parolaparken"/>
				<XTRA name="digistop_id" val="1013"/>
			</STOP>
			<SHAPE time="2" dist="265.827">
3239895.0 6718403.0 `` 0
3240137.0 6718293.0 `` 0
			</SHAPE>
			<STOP code="2:1014" x="3240137.0" y="6718293.0" id="17" ord="41">
				<ARRIVAL date="20140402" time="1214"/>
				<DEPARTURE date="20140402" time="1214"/>
				<NAME lang="1" val="Kiikku"/>
				<NAME lang="2" val="Kiikku"/>
				<XTRA name="digistop_id" val="1014"/>
			</STOP>
		</LINE>
		<WALK>
			<LENGTH time="0.109" dist="11.494"/>
			<STOP code="2:1014" x="3240137.0" y="6718293.0" id="17">
				<ARRIVAL date="20140402" time="1214"/>
				<DEPARTURE date="20140402" time="1214"/>
				<NAME lang="1" val="Kiikku"/>
				<NAME lang="2" val="Kiikku"/>
				<XTRA name="digistop_id" val="1014"/>
			</STOP>
			<SHAPE time="0" dist="11.494">
3240139.7 6718294.0 `` 0
3240137.0 6718301.2 `` 0
			</SHAPE>
			<POINT uid="end" x="3240138.0" y="6718301.5">
				<ARRIVAL date="20140402" time="1214"/>
				<DEPARTURE date="20140402" time="1215"/>
			</POINT>
		</WALK>
		<POINT uid="end" x="3240138.0" y="6718301.5">
			<ARRIVAL date="20140402" time="1214"/>
			<DEPARTURE date="20140402" time="1215"/>
		</POINT>
	</ROUTE>
	<ROUTE from="start" to="end">
		<LENGTH time="14.199" dist="5397.238"/>
		<POINT uid="start" x="3239920.8" y="6714163.5">
			<ARRIVAL date="20140402" time="1207"/>
			<DEPARTURE date="20140402" time="1208"/>
		</POINT>
		<WALK>
			<LENGTH time="1.090" dist="88.535"/>
			<POINT uid="start" x="3239920.8" y="6714163.5">
				<ARRIVAL date="20140402" time="1207"/>
				<DEPARTURE date="20140402" time="1208"/>
			</POINT>
			<SHAPE time="0" dist="29.258">
3239920.0 6714163.0 `` 0
3239905.3 6714187.3 `` 0
			</SHAPE>
			<MAPLOC x="3239905.3" y="6714187.3" type="12131">
				<ARRIVAL date="20140402" time="1208"/>
				<DEPARTURE date="20140402" time="1209"/>
				<NAME lang="1" val="Maariankatu"/>
			</MAPLOC>
			<SHAPE time="1" dist="59.277">
3239905.3 6714187.3 `` 0
3239864.2 6714162.7 `` 0
			</SHAPE>
			<STOP code="2:472" x="3239870.0" y="6714153.0" id="1229">
				<ARRIVAL date="20140402" time="1209"/>
				<DEPARTURE date="20140402" time="1209"/>
				<NAME lang="1" val="Puutori"/>
				<NAME lang="2" val="Cygnaeus skola"/>
				<XTRA name="digistop_id" val="472"/>
			</STOP>
		</WALK>
		<LINE id="1048" code="18" type="1" mobility="0">
			<LENGTH time="13.000" dist="5297.209"/>
			<STOP code="2:472" x="3239870.0" y="6714153.0" id="1229" ord="27">
				<ARRIVAL date="20140402" time="1209"/>
				<DEPARTURE date="20140402" time="1209"/>
				<NAME lang="1" val="Puutori"/>
				<NAME lang="2" val="Cygnaeus skola"/>
				<XTRA name="digistop_id" val="472"/>
			</STOP>
			<SHAPE time="1" dist="349.860">
3239870.0 6714153.0 `` 0
3239989.0 6714482.0 `` 0
			</SHAPE>
			<STOP code="2:19" x="3239989.0" y="6714482.0" id="845">
				<ARRIVAL date="20140402" time="1210"/>
				<DEPARTURE date="20140402" time="1210"/>
				<NAME lang="1" val="Linja-autoasema"/>
				<NAME lang="2" val="Linjebilstationen"/>
				<XTRA name="digistop_id" val="19"/>
			</STOP>
			<SHAPE time="1" dist="449.694">
3239989.0 6714482.0 `` 0
3239950.0 6714930.0 `` 0
			</SHAPE>
			<STOP code="2:174" x="3239950.0" y="6714930.0" id="729">
				<ARRIVAL date="20140402" time="1211"/>
				<DEPARTURE date="20140402" time="1211"/>
				<NAME lang="1" val="Autistenaukio"/>
				<NAME lang="2" val="Autisplan"/>
				<XTRA name="digistop_id" val="174"/>
			</STOP>
			<SHAPE time="1" dist="186.657">
3239950.0 6714930.0 `` 0
3240054.0 6715085.0 `` 0
			</SHAPE>
			<STOP code="2:175" x="3240054.0" y="6715085.0" id="740">
				<ARRIVAL date="20140402" time="1212"/>
				<DEPARTURE date="20140402" time="1212"/>
				<NAME lang="1" val="Oskarinkuja"/>
				<NAME lang="2" val="Oskarsgränd"/>
				<XTRA name="digistop_id" val="175"/>
			</STOP>
			<SHAPE time="0" dist="287.127">
3240054.0 6715085.0 `` 0
3240113.0 6715366.0 `` 0
			</SHAPE>
			<STOP code="2:612" x="3240113.0" y="6715366.0" id="1390">
				<ARRIVAL date="20140402" time="1212"/>
				<DEPARTURE date="20140402" time="1212"/>
				<NAME lang="1" val="Kastuntie"/>
				<NAME lang="2" val="Kastuvägen"/>
				<XTRA name="digistop_id" val="612"/>
			</STOP>
			<SHAPE time="1" dist="463.341">
3240113.0 6715366.0 `` 0
3239974.0 6715808.0 `` 0
			</SHAPE>
			<STOP code="2:613" x="3239974.0" y="6715808.0" id="1391">
				<ARRIVAL date="20140402" time="1213"/>
				<DEPARTURE date="20140402" time="1213"/>
				<NAME lang="1" val="Parrantie"/>
				<NAME lang="2" val="Partavägen"/>
				<XTRA name="digistop_id" val="613"/>
			</STOP>
			<SHAPE time="2" dist="768.500">
3239974.0 6715808.0 `` 0
3240022.0 6716575.0 `` 0
			</SHAPE>
			<STOP code="2:979" x="3240022.0" y="6716575.0" id="1741">
				<ARRIVAL date="20140402" time="1215"/>
				<DEPARTURE date="20140402" time="1215"/>
				<NAME lang="1" val="Markulanpuisto"/>
				<NAME lang="2" val="Markulaparken"/>
				<XTRA name="digistop_id" val="979"/>
			</STOP>
			<SHAPE time="0" dist="296.061">
3240022.0 6716575.0 `` 0
3240156.0 6716839.0 `` 0
			</SHAPE>
			<STOP code="2:980" x="3240156.0" y="6716839.0" id="1743">
				<ARRIVAL date="20140402" time="1215"/>
				<DEPARTURE date="20140402" time="1215"/>
				<NAME lang="1" val="Toukolanpuistikko"/>
				<NAME lang="2" val="Toukolaskvären"/>
				<XTRA name="digistop_id" val="980"/>
			</STOP>
			<SHAPE time="1" dist="621.007">
3240156.0 6716839.0 `` 0
3240327.0 6717436.0 `` 0
			</SHAPE>
			<STOP code="2:981" x="3240327.0" y="6717436.0" id="1744">
				<ARRIVAL date="20140402" time="1216"/>
				<DEPARTURE date="20140402" time="1216"/>
				<NAME lang="1" val="Palli"/>
				<NAME lang="2" val="Palli"/>
				<XTRA name="digistop_id" val="981"/>
			</STOP>
			<SHAPE time="1" dist="385.251">
3240327.0 6717436.0 `` 0
3240070.0 6717723.0 `` 0
			</SHAPE>
			<STOP code="2:982" x="3240070.0" y="6717723.0" id="1745">
				<ARRIVAL date="20140402" time="1217"/>
				<DEPARTURE date="20140402" time="1217"/>
				<NAME lang="1" val="Runosmäen terveysasema"/>
				<NAME lang="2" val="Runosmäen terveysasema"/>
				<XTRA name="digistop_id" val="982"/>
			</STOP>
			<SHAPE time="1" dist="342.286">
3240070.0 6717723.0 `` 0
3239732.0 6717777.0 `` 0
			</SHAPE>
			<STOP code="2:984" x="3239732.0" y="6717777.0" id="1747">
				<ARRIVAL date="20140402" time="1218"/>
				<DEPARTURE date="20140402" time="1218"/>
				<NAME lang="1" val="Signalistinpolku"/>
				<NAME lang="2" val="Signaliststigen"/>
				<XTRA name="digistop_id" val="984"/>
			</STOP>
			<SHAPE time="1" dist="233.225">
3239732.0 6717777.0 `` 0
3239637.0 6717990.0 `` 0
			</SHAPE>
			<STOP code="2:985" x="3239637.0" y="6717990.0" id="1748">
				<ARRIVAL date="20140402" time="1219"/>
				<DEPARTURE date="20140402" time="1219"/>
				<NAME lang="1" val="Munterinkatu"/>
				<NAME lang="2" val="Muntersgatan"/>
				<XTRA name="digistop_id" val="985"/>
			</STOP>
			<SHAPE time="0" dist="241.661">
3239637.0 6717990.0 `` 0
3239537.0 6718210.0 `` 0
			</SHAPE>
			<STOP code="2:986" x="3239537.0" y="6718210.0" id="1749">
				<ARRIVAL date="20140402" time="1219"/>
				<DEPARTURE date="20140402" time="1219"/>
				<NAME lang="1" val="Nostoväenkatu"/>
				<NAME lang="2" val="Lantvärnsgatan"/>
				<XTRA name="digistop_id" val="986"/>
			</STOP>
			<SHAPE time="1" dist="406.710">
3239537.0 6718210.0 `` 0
3239895.0 6718403.0 `` 0
			</SHAPE>
			<STOP code="2:1013" x="3239895.0" y="6718403.0" id="16">
				<ARRIVAL date="20140402" time="1220"/>
				<DEPARTURE date="20140402" time="1220"/>
				<NAME lang="1" val="Parolanpuisto"/>
				<NAME lang="2" val="Parolaparken"/>
				<XTRA name="digistop_id" val="1013"/>
			</STOP>
			<SHAPE time="2" dist="265.827">
3239895.0 6718403.0 `` 0
3240137.0 6718293.0 `` 0
			</SHAPE>
			<STOP code="2:1014" x="3240137.0" y="6718293.0" id="17" ord="41">
				<ARRIVAL date="20140402" time="1222"/>
				<DEPARTURE date="20140402" time="1222"/>
				<NAME lang="1" val="Kiikku"/>
				<NAME lang="2" val="Kiikku"/>
				<XTRA name="digistop_id" val="1014"/>
			</STOP>
		</LINE>
		<WALK>
			<LENGTH time="0.109" dist="11.494"/>
			<STOP code="2:1014" x="3240137.0" y="6718293.0" id="17">
				<ARRIVAL date="20140402" time="1222"/>
				<DEPARTURE date="20140402" time="1222"/>
				<NAME lang="1" val="Kiikku"/>
				<NAME lang="2" val="Kiikku"/>
				<XTRA name="digistop_id" val="1014"/>
			</STOP>
			<SHAPE time="0" dist="11.494">
3240139.7 6718294.0 `` 0
3240137.0 6718301.2 `` 0
			</SHAPE>
			<POINT uid="end" x="3240138.0" y="6718301.5">
				<ARRIVAL date="20140402" time="1222"/>
				<DEPARTURE date="20140402" time="1223"/>
			</POINT>
		</WALK>
		<POINT uid="end" x="3240138.0" y="6718301.5">
			<ARRIVAL date="20140402" time="1222"/>
			<DEPARTURE date="20140402" time="1223"/>
		</POINT>
	</ROUTE>
	<ROUTE from="start" to="end">
		<LENGTH time="14.199" dist="5397.238"/>
		<POINT uid="start" x="3239920.8" y="6714163.5">
			<ARRIVAL date="20140402" time="1214"/>
			<DEPARTURE date="20140402" time="1215"/>
		</POINT>
		<WALK>
			<LENGTH time="1.090" dist="88.535"/>
			<POINT uid="start" x="3239920.8" y="6714163.5">
				<ARRIVAL date="20140402" time="1214"/>
				<DEPARTURE date="20140402" time="1215"/>
			</POINT>
			<SHAPE time="0" dist="29.258">
3239920.0 6714163.0 `` 0
3239905.3 6714187.3 `` 0
			</SHAPE>
			<MAPLOC x="3239905.3" y="6714187.3" type="12131">
				<ARRIVAL date="20140402" time="1215"/>
				<DEPARTURE date="20140402" time="1216"/>
				<NAME lang="1" val="Maariankatu"/>
			</MAPLOC>
			<SHAPE time="1" dist="59.277">
3239905.3 6714187.3 `` 0
3239864.2 6714162.7 `` 0
			</SHAPE>
			<STOP code="2:472" x="3239870.0" y="6714153.0" id="1229">
				<ARRIVAL date="20140402" time="1216"/>
				<DEPARTURE date="20140402" time="1216"/>
				<NAME lang="1" val="Puutori"/>
				<NAME lang="2" val="Cygnaeus skola"/>
				<XTRA name="digistop_id" val="472"/>
			</STOP>
		</WALK>
		<LINE id="1067" code="18" type="1" mobility="0">
			<LENGTH time="13.000" dist="5297.209"/>
			<STOP code="2:472" x="3239870.0" y="6714153.0" id="1229" ord="27">
				<ARRIVAL date="20140402" time="1216"/>
				<DEPARTURE date="20140402" time="1216"/>
				<NAME lang="1" val="Puutori"/>
				<NAME lang="2" val="Cygnaeus skola"/>
				<XTRA name="digistop_id" val="472"/>
			</STOP>
			<SHAPE time="1" dist="349.860">
3239870.0 6714153.0 `` 0
3239989.0 6714482.0 `` 0
			</SHAPE>
			<STOP code="2:19" x="3239989.0" y="6714482.0" id="845">
				<ARRIVAL date="20140402" time="1217"/>
				<DEPARTURE date="20140402" time="1217"/>
				<NAME lang="1" val="Linja-autoasema"/>
				<NAME lang="2" val="Linjebilstationen"/>
				<XTRA name="digistop_id" val="19"/>
			</STOP>
			<SHAPE time="1" dist="449.694">
3239989.0 6714482.0 `` 0
3239950.0 6714930.0 `` 0
			</SHAPE>
			<STOP code="2:174" x="3239950.0" y="6714930.0" id="729">
				<ARRIVAL date="20140402" time="1218"/>
				<DEPARTURE date="20140402" time="1218"/>
				<NAME lang="1" val="Autistenaukio"/>
				<NAME lang="2" val="Autisplan"/>
				<XTRA name="digistop_id" val="174"/>
			</STOP>
			<SHAPE time="1" dist="186.657">
3239950.0 6714930.0 `` 0
3240054.0 6715085.0 `` 0
			</SHAPE>
			<STOP code="2:175" x="3240054.0" y="6715085.0" id="740">
				<ARRIVAL date="20140402" time="1219"/>
				<DEPARTURE date="20140402" time="1219"/>
				<NAME lang="1" val="Oskarinkuja"/>
				<NAME lang="2" val="Oskarsgränd"/>
				<XTRA name="digistop_id" val="175"/>
			</STOP>
			<SHAPE time="0" dist="287.127">
3240054.0 6715085.0 `` 0
3240113.0 6715366.0 `` 0
			</SHAPE>
			<STOP code="2:612" x="3240113.0" y="6715366.0" id="1390">
				<ARRIVAL date="20140402" time="1219"/>
				<DEPARTURE date="20140402" time="1219"/>
				<NAME lang="1" val="Kastuntie"/>
				<NAME lang="2" val="Kastuvägen"/>
				<XTRA name="digistop_id" val="612"/>
			</STOP>
			<SHAPE time="1" dist="463.341">
3240113.0 6715366.0 `` 0
3239974.0 6715808.0 `` 0
			</SHAPE>
			<STOP code="2:613" x="3239974.0" y="6715808.0" id="1391">
				<ARRIVAL date="20140402" time="1220"/>
				<DEPARTURE date="20140402" time="1220"/>
				<NAME lang="1" val="Parrantie"/>
				<NAME lang="2" val="Partavägen"/>
				<XTRA name="digistop_id" val="613"/>
			</STOP>
			<SHAPE time="2" dist="768.500">
3239974.0 6715808.0 `` 0
3240022.0 6716575.0 `` 0
			</SHAPE>
			<STOP code="2:979" x="3240022.0" y="6716575.0" id="1741">
				<ARRIVAL date="20140402" time="1222"/>
				<DEPARTURE date="20140402" time="1222"/>
				<NAME lang="1" val="Markulanpuisto"/>
				<NAME lang="2" val="Markulaparken"/>
				<XTRA name="digistop_id" val="979"/>
			</STOP>
			<SHAPE time="0" dist="296.061">
3240022.0 6716575.0 `` 0
3240156.0 6716839.0 `` 0
			</SHAPE>
			<STOP code="2:980" x="3240156.0" y="6716839.0" id="1743">
				<ARRIVAL date="20140402" time="1222"/>
				<DEPARTURE date="20140402" time="1222"/>
				<NAME lang="1" val="Toukolanpuistikko"/>
				<NAME lang="2" val="Toukolaskvären"/>
				<XTRA name="digistop_id" val="980"/>
			</STOP>
			<SHAPE time="1" dist="621.007">
3240156.0 6716839.0 `` 0
3240327.0 6717436.0 `` 0
			</SHAPE>
			<STOP code="2:981" x="3240327.0" y="6717436.0" id="1744">
				<ARRIVAL date="20140402" time="1223"/>
				<DEPARTURE date="20140402" time="1223"/>
				<NAME lang="1" val="Palli"/>
				<NAME lang="2" val="Palli"/>
				<XTRA name="digistop_id" val="981"/>
			</STOP>
			<SHAPE time="1" dist="385.251">
3240327.0 6717436.0 `` 0
3240070.0 6717723.0 `` 0
			</SHAPE>
			<STOP code="2:982" x="3240070.0" y="6717723.0" id="1745">
				<ARRIVAL date="20140402" time="1224"/>
				<DEPARTURE date="20140402" time="1224"/>
				<NAME lang="1" val="Runosmäen terveysasema"/>
				<NAME lang="2" val="Runosmäen terveysasema"/>
				<XTRA name="digistop_id" val="982"/>
			</STOP>
			<SHAPE time="1" dist="342.286">
3240070.0 6717723.0 `` 0
3239732.0 6717777.0 `` 0
			</SHAPE>
			<STOP code="2:984" x="3239732.0" y="6717777.0" id="1747">
				<ARRIVAL date="20140402" time="1225"/>
				<DEPARTURE date="20140402" time="1225"/>
				<NAME lang="1" val="Signalistinpolku"/>
				<NAME lang="2" val="Signaliststigen"/>
				<XTRA name="digistop_id" val="984"/>
			</STOP>
			<SHAPE time="1" dist="233.225">
3239732.0 6717777.0 `` 0
3239637.0 6717990.0 `` 0
			</SHAPE>
			<STOP code="2:985" x="3239637.0" y="6717990.0" id="1748">
				<ARRIVAL date="20140402" time="1226"/>
				<DEPARTURE date="20140402" time="1226"/>
				<NAME lang="1" val="Munterinkatu"/>
				<NAME lang="2" val="Muntersgatan"/>
				<XTRA name="digistop_id" val="985"/>
			</STOP>
			<SHAPE time="0" dist="241.661">
3239637.0 6717990.0 `` 0
3239537.0 6718210.0 `` 0
			</SHAPE>
			<STOP code="2:986" x="3239537.0" y="6718210.0" id="1749">
				<ARRIVAL date="20140402" time="1226"/>
				<DEPARTURE date="20140402" time="1226"/>
				<NAME lang="1" val="Nostoväenkatu"/>
				<NAME lang="2" val="Lantvärnsgatan"/>
				<XTRA name="digistop_id" val="986"/>
			</STOP>
			<SHAPE time="1" dist="406.710">
3239537.0 6718210.0 `` 0
3239895.0 6718403.0 `` 0
			</SHAPE>
			<STOP code="2:1013" x="3239895.0" y="6718403.0" id="16">
				<ARRIVAL date="20140402" time="1227"/>
				<DEPARTURE date="20140402" time="1227"/>
				<NAME lang="1" val="Parolanpuisto"/>
				<NAME lang="2" val="Parolaparken"/>
				<XTRA name="digistop_id" val="1013"/>
			</STOP>
			<SHAPE time="2" dist="265.827">
3239895.0 6718403.0 `` 0
3240137.0 6718293.0 `` 0
			</SHAPE>
			<STOP code="2:1014" x="3240137.0" y="6718293.0" id="17" ord="41">
				<ARRIVAL date="20140402" time="1229"/>
				<DEPARTURE date="20140402" time="1229"/>
				<NAME lang="1" val="Kiikku"/>
				<NAME lang="2" val="Kiikku"/>
				<XTRA name="digistop_id" val="1014"/>
			</STOP>
		</LINE>
		<WALK>
			<LENGTH time="0.109" dist="11.494"/>
			<STOP code="2:1014" x="3240137.0" y="6718293.0" id="17">
				<ARRIVAL date="20140402" time="1229"/>
				<DEPARTURE date="20140402" time="1229"/>
				<NAME lang="1" val="Kiikku"/>
				<NAME lang="2" val="Kiikku"/>
				<XTRA name="digistop_id" val="1014"/>
			</STOP>
			<SHAPE time="0" dist="11.494">
3240139.7 6718294.0 `` 0
3240137.0 6718301.2 `` 0
			</SHAPE>
			<POINT uid="end" x="3240138.0" y="6718301.5">
				<ARRIVAL date="20140402" time="1229"/>
				<DEPARTURE date="20140402" time="1230"/>
			</POINT>
		</WALK>
		<POINT uid="end" x="3240138.0" y="6718301.5">
			<ARRIVAL date="20140402" time="1229"/>
			<DEPARTURE date="20140402" time="1230"/>
		</POINT>
	</ROUTE>
	<ROUTE from="start" to="end">
		<LENGTH time="14.199" dist="5397.238"/>
		<POINT uid="start" x="3239920.8" y="6714163.5">
			<ARRIVAL date="20140402" time="1222"/>
			<DEPARTURE date="20140402" time="1223"/>
		</POINT>
		<WALK>
			<LENGTH time="1.090" dist="88.535"/>
			<POINT uid="start" x="3239920.8" y="6714163.5">
				<ARRIVAL date="20140402" time="1222"/>
				<DEPARTURE date="20140402" time="1223"/>
			</POINT>
			<SHAPE time="0" dist="29.258">
3239920.0 6714163.0 `` 0
3239905.3 6714187.3 `` 0
			</SHAPE>
			<MAPLOC x="3239905.3" y="6714187.3" type="12131">
				<ARRIVAL date="20140402" time="1223"/>
				<DEPARTURE date="20140402" time="1224"/>
				<NAME lang="1" val="Maariankatu"/>
			</MAPLOC>
			<SHAPE time="1" dist="59.277">
3239905.3 6714187.3 `` 0
3239864.2 6714162.7 `` 0
			</SHAPE>
			<STOP code="2:472" x="3239870.0" y="6714153.0" id="1229">
				<ARRIVAL date="20140402" time="1224"/>
				<DEPARTURE date="20140402" time="1224"/>
				<NAME lang="1" val="Puutori"/>
				<NAME lang="2" val="Cygnaeus skola"/>
				<XTRA name="digistop_id" val="472"/>
			</STOP>
		</WALK>
		<LINE id="1089" code="18" type="1" mobility="0">
			<LENGTH time="13.000" dist="5297.209"/>
			<STOP code="2:472" x="3239870.0" y="6714153.0" id="1229" ord="27">
				<ARRIVAL date="20140402" time="1224"/>
				<DEPARTURE date="20140402" time="1224"/>
				<NAME lang="1" val="Puutori"/>
				<NAME lang="2" val="Cygnaeus skola"/>
				<XTRA name="digistop_id" val="472"/>
			</STOP>
			<SHAPE time="1" dist="349.860">
3239870.0 6714153.0 `` 0
3239989.0 6714482.0 `` 0
			</SHAPE>
			<STOP code="2:19" x="3239989.0" y="6714482.0" id="845">
				<ARRIVAL date="20140402" time="1225"/>
				<DEPARTURE date="20140402" time="1225"/>
				<NAME lang="1" val="Linja-autoasema"/>
				<NAME lang="2" val="Linjebilstationen"/>
				<XTRA name="digistop_id" val="19"/>
			</STOP>
			<SHAPE time="1" dist="449.694">
3239989.0 6714482.0 `` 0
3239950.0 6714930.0 `` 0
			</SHAPE>
			<STOP code="2:174" x="3239950.0" y="6714930.0" id="729">
				<ARRIVAL date="20140402" time="1226"/>
				<DEPARTURE date="20140402" time="1226"/>
				<NAME lang="1" val="Autistenaukio"/>
				<NAME lang="2" val="Autisplan"/>
				<XTRA name="digistop_id" val="174"/>
			</STOP>
			<SHAPE time="1" dist="186.657">
3239950.0 6714930.0 `` 0
3240054.0 6715085.0 `` 0
			</SHAPE>
			<STOP code="2:175" x="3240054.0" y="6715085.0" id="740">
				<ARRIVAL date="20140402" time="1227"/>
				<DEPARTURE date="20140402" time="1227"/>
				<NAME lang="1" val="Oskarinkuja"/>
				<NAME lang="2" val="Oskarsgränd"/>
				<XTRA name="digistop_id" val="175"/>
			</STOP>
			<SHAPE time="0" dist="287.127">
3240054.0 6715085.0 `` 0
3240113.0 6715366.0 `` 0
			</SHAPE>
			<STOP code="2:612" x="3240113.0" y="6715366.0" id="1390">
				<ARRIVAL date="20140402" time="1227"/>
				<DEPARTURE date="20140402" time="1227"/>
				<NAME lang="1" val="Kastuntie"/>
				<NAME lang="2" val="Kastuvägen"/>
				<XTRA name="digistop_id" val="612"/>
			</STOP>
			<SHAPE time="1" dist="463.341">
3240113.0 6715366.0 `` 0
3239974.0 6715808.0 `` 0
			</SHAPE>
			<STOP code="2:613" x="3239974.0" y="6715808.0" id="1391">
				<ARRIVAL date="20140402" time="1228"/>
				<DEPARTURE date="20140402" time="1228"/>
				<NAME lang="1" val="Parrantie"/>
				<NAME lang="2" val="Partavägen"/>
				<XTRA name="digistop_id" val="613"/>
			</STOP>
			<SHAPE time="2" dist="768.500">
3239974.0 6715808.0 `` 0
3240022.0 6716575.0 `` 0
			</SHAPE>
			<STOP code="2:979" x="3240022.0" y="6716575.0" id="1741">
				<ARRIVAL date="20140402" time="1230"/>
				<DEPARTURE date="20140402" time="1230"/>
				<NAME lang="1" val="Markulanpuisto"/>
				<NAME lang="2" val="Markulaparken"/>
				<XTRA name="digistop_id" val="979"/>
			</STOP>
			<SHAPE time="0" dist="296.061">
3240022.0 6716575.0 `` 0
3240156.0 6716839.0 `` 0
			</SHAPE>
			<STOP code="2:980" x="3240156.0" y="6716839.0" id="1743">
				<ARRIVAL date="20140402" time="1230"/>
				<DEPARTURE date="20140402" time="1230"/>
				<NAME lang="1" val="Toukolanpuistikko"/>
				<NAME lang="2" val="Toukolaskvären"/>
				<XTRA name="digistop_id" val="980"/>
			</STOP>
			<SHAPE time="1" dist="621.007">
3240156.0 6716839.0 `` 0
3240327.0 6717436.0 `` 0
			</SHAPE>
			<STOP code="2:981" x="3240327.0" y="6717436.0" id="1744">
				<ARRIVAL date="20140402" time="1231"/>
				<DEPARTURE date="20140402" time="1231"/>
				<NAME lang="1" val="Palli"/>
				<NAME lang="2" val="Palli"/>
				<XTRA name="digistop_id" val="981"/>
			</STOP>
			<SHAPE time="1" dist="385.251">
3240327.0 6717436.0 `` 0
3240070.0 6717723.0 `` 0
			</SHAPE>
			<STOP code="2:982" x="3240070.0" y="6717723.0" id="1745">
				<ARRIVAL date="20140402" time="1232"/>
				<DEPARTURE date="20140402" time="1232"/>
				<NAME lang="1" val="Runosmäen terveysasema"/>
				<NAME lang="2" val="Runosmäen terveysasema"/>
				<XTRA name="digistop_id" val="982"/>
			</STOP>
			<SHAPE time="1" dist="342.286">
3240070.0 6717723.0 `` 0
3239732.0 6717777.0 `` 0
			</SHAPE>
			<STOP code="2:984" x="3239732.0" y="6717777.0" id="1747">
				<ARRIVAL date="20140402" time="1233"/>
				<DEPARTURE date="20140402" time="1233"/>
				<NAME lang="1" val="Signalistinpolku"/>
				<NAME lang="2" val="Signaliststigen"/>
				<XTRA name="digistop_id" val="984"/>
			</STOP>
			<SHAPE time="1" dist="233.225">
3239732.0 6717777.0 `` 0
3239637.0 6717990.0 `` 0
			</SHAPE>
			<STOP code="2:985" x="3239637.0" y="6717990.0" id="1748">
				<ARRIVAL date="20140402" time="1234"/>
				<DEPARTURE date="20140402" time="1234"/>
				<NAME lang="1" val="Munterinkatu"/>
				<NAME lang="2" val="Muntersgatan"/>
				<XTRA name="digistop_id" val="985"/>
			</STOP>
			<SHAPE time="0" dist="241.661">
3239637.0 6717990.0 `` 0
3239537.0 6718210.0 `` 0
			</SHAPE>
			<STOP code="2:986" x="3239537.0" y="6718210.0" id="1749">
				<ARRIVAL date="20140402" time="1234"/>
				<DEPARTURE date="20140402" time="1234"/>
				<NAME lang="1" val="Nostoväenkatu"/>
				<NAME lang="2" val="Lantvärnsgatan"/>
				<XTRA name="digistop_id" val="986"/>
			</STOP>
			<SHAPE time="1" dist="406.710">
3239537.0 6718210.0 `` 0
3239895.0 6718403.0 `` 0
			</SHAPE>
			<STOP code="2:1013" x="3239895.0" y="6718403.0" id="16">
				<ARRIVAL date="20140402" time="1235"/>
				<DEPARTURE date="20140402" time="1235"/>
				<NAME lang="1" val="Parolanpuisto"/>
				<NAME lang="2" val="Parolaparken"/>
				<XTRA name="digistop_id" val="1013"/>
			</STOP>
			<SHAPE time="2" dist="265.827">
3239895.0 6718403.0 `` 0
3240137.0 6718293.0 `` 0
			</SHAPE>
			<STOP code="2:1014" x="3240137.0" y="6718293.0" id="17" ord="41">
				<ARRIVAL date="20140402" time="1237"/>
				<DEPARTURE date="20140402" time="1237"/>
				<NAME lang="1" val="Kiikku"/>
				<NAME lang="2" val="Kiikku"/>
				<XTRA name="digistop_id" val="1014"/>
			</STOP>
		</LINE>
		<WALK>
			<LENGTH time="0.109" dist="11.494"/>
			<STOP code="2:1014" x="3240137.0" y="6718293.0" id="17">
				<ARRIVAL date="20140402" time="1237"/>
				<DEPARTURE date="20140402" time="1237"/>
				<NAME lang="1" val="Kiikku"/>
				<NAME lang="2" val="Kiikku"/>
				<XTRA name="digistop_id" val="1014"/>
			</STOP>
			<SHAPE time="0" dist="11.494">
3240139.7 6718294.0 `` 0
3240137.0 6718301.2 `` 0
			</SHAPE>
			<POINT uid="end" x="3240138.0" y="6718301.5">
				<ARRIVAL date="20140402" time="1237"/>
				<DEPARTURE date="20140402" time="1238"/>
			</POINT>
		</WALK>
		<POINT uid="end" x="3240138.0" y="6718301.5">
			<ARRIVAL date="20140402" time="1237"/>
			<DEPARTURE date="20140402" time="1238"/>
		</POINT>
	</ROUTE>
</MTRXML>

```

<%= headers 200 %>
<%= json(:gist_comment) { |h| [h] } %>

### Lines
List of available lines;Askainen, Granvik, Helsinki, Hirvikoski, Houtskari, Huittinen, Karjala, Kemiö, Kittuis/Galtby, Korppoo, Koski TL, Kustavi, Kyrö, Laajoki, Lemu th, Lielahti, Livonsaari, Loimaa, Masku, Miiainen, Mossala, Mynämäki, Nousiainen, Ohensaari, Oripää, P1, P2, P3, Paimio, Paimio motelli, Palv., Parainen, Rantola, Rauma, Salo, Sauvo, Sauvo th, Sydmo, Taalintehdas, Tampere, Teersalo, Turku, Uusikaupunki, Valpperi, tien/Kustavintien risteys, 1, 01, 2, 2A, 3, 4, 6, 8, 9, 11, 11A, 12, 13, 14, 15, 18, 20, 21, 22, 23, 28, 30, 31, 32, 33, 34, 36, 40, 42, 50, 51, 52, 53, 54, 55, 56, 58, 61, 66, 67, 72, 73, 74, 80, 83, 88, 90, 91, 99, 100, 109, 110, 111, 112, 115, 116, 118, 119, 191, 192, 194, 195, 201, 211, 212, 213, 221, 222, 223, 224, 231, 232, 280, 282, 285, 320, 321, 420, 422, 429

## Geocoding

    GET /geocode.php

### Response

<%= headers 200 %>
<%= json :gist_comment %>


    application/vnd.github.VERSION.raw+json
    application/vnd.github.VERSION.text+json
    application/vnd.github.VERSION.html+json
    application/vnd.github.VERSION.full+json
