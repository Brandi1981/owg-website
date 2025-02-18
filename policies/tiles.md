---
title: Tile Usage Policy
permalink: /policies/tiles/
---

# {{ page.title }}

We are in principle happy for our map tiles to be used by external users for creative and unexpected uses – in contrast to most web mapping providers, which insist that you use only their supplied API.

However, **OpenStreetMap's own servers are run entirely on donated resources.** They have strictly limited capacity. Heavy use of OSM tiles adversely affects people's ability to edit the map, and is an abuse of the individual donations and sponsorship which provide hardware and bandwidth. As a result, we require that users of the tiles abide by this tile usage policy.

**OpenStreetMap data is [free for everyone to use](https://wiki.openstreetmap.org/wiki/OpenStreetMap_License). Our tile servers are not.**

Below are the minimum requirements that users of tile.openstreetmap.org must adhere to. These may change in future, depending on available resources. Should any users or patterns of usage nevertheless cause problems to the service, access may still be blocked without prior notice. We will try to contact relevant parties if possible, but cannot guarantee this.

But because OpenStreetMap data is free, many other organisations provide map tiles made from OSM data. If your project doesn't meet these requirements, you can get OSM-derived map tiles elsewhere.

Use of any OSMF provided service is further governed by the [OSMF Terms of Use](https://wiki.osmfoundation.org/wiki/Terms_of_Use).

## Requirements

* Heavy use (e.g. distributing an app that uses tiles from openstreetmap.org) is **forbidden** without prior permission from the [Operations Working Group](https://wiki.osmfoundation.org/wiki/Operations_Working_Group). See below for alternatives.
* Clearly display [license](https://wiki.openstreetmap.org/wiki/License) [attribution](https://wiki.osmfoundation.org/wiki/Licence/Attribution_Guidelines).
* Do not actively or passively encourage copyright infringement.
* Recommended: Do not hardcode any URL at tile.openstreetmap.org as doing so will limit your ability to react quickly if the service is disrupted or blocked.
* Recommended: add a link to [https://www.openstreetmap.org/fixthemap](https://www.openstreetmap.org/fixthemap) to allow your users to report and fix problems in our data.

## Technical Usage Requirements

* **Valid [HTTP User-Agent](http://en.wikipedia.org/wiki/en:User_agent)** identifying application. Faking another app's User-Agent WILL get you blocked.
* If known, a **valid [HTTP Referer](http://en.wikipedia.org/wiki/en:HTTP_Referer)**.
* **DO NOT send no-cache headers**. ("Cache-Control: no-cache", "Pragma: no-cache" etc.)
* **Cache Tile** downloads locally according to HTTP Expiry Header, alternatively a minimum of 7 days.
* **Maximum of 2 download threads**. (Unmodified web browsers' download thread limits are acceptable.)

Note: modern web browsers in standard configuration generally pass all the above technical requirements.

## Bulk Downloading

Bulk downloading is **strongly discouraged**. Do not download [tiles](https://wiki.openstreetmap.org/wiki/Tiles) unnecessarily.

In particular, downloading an area of over 250 tiles at zoom level 13 or higher for offline or later usage is **forbidden**. These tiles are generally not available (cached) on the server in advance, and have to be rendered specifically for those requests, putting an unjustified burden on the available resources.

## Privacy

Use of all services is subject to the [OpenStreetMap Foundation privacy policy](http://wiki.osmfoundation.org/wiki/Privacy_Policy). Please do not submit personal data or other confidential material to any of our services.

## Changes to this policy

This policy may change at any time subject to the needs and constraints of the project. Commercial services, or those that seek donations, should be especially aware that access may be withdrawn at any point: you may no longer be able to serve your paying customers if access is withdrawn.

## Alternative OpenStreetMap Tile Providers

Tile servers based on OSM data:

* [Wiki tile server list](https://wiki.openstreetmap.org/wiki/Tile_servers)
* [Wiki TMS page](https://wiki.openstreetmap.org/wiki/TMS)

Paid-for tile servers:

* See [Commercial OSM Software and Services](https://wiki.openstreetmap.org/wiki/Commercial_OSM_Software_and_Services)

Setting up your own tile server:

* [the switch2osm website, with up to date information on running your own OSM based services](http://switch2osm.org/)

------

*This policy relates to the Standard ("Mapnik") tiles rendered and served by {a,b,c}.**tile.openstreetmap.org** as part of the OpenStreetMap project. It does not relate to other tiles that are viewable on the OpenStreetMap.org homepage, which may have their own usage policies. You should contact the individual projects, such as [OpenCycleMap](https://wiki.openstreetmap.org/wiki/OpenCycleMap), if you wish to use their tiles.*
