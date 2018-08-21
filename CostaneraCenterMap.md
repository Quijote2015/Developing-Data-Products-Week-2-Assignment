---
title: "Interactive Map for Costanera Center in Santiago, Chile"
author: "Cristian Gutierrez"
date: "21 de agosto de 2018"
output: 
  html_document: 
    fig_caption: yes
    keep_md: yes
---



Developing Data Products-Week 2-Assignment
My First Map
Let's create a map that shows the Costanera Center in Santiago of Chile.
To do that, let's first load the library Leaflet.


```r
library(leaflet)
```

Create the map of Santiago, Chile.


```r
my_map <- leaflet() %>%
  addTiles()
my_map
```

Create a link to the office site of Costanera center, which we could get relevant information.

```r
CostaneraCenter <- c("<a href= 'http://mall.costaneracenter.cl/#map1' >Costanera Center</a>")
leaflet() %>%
  addTiles() %>%
  addMarkers(lat=-33.417993, lng=-70.606390, popup = CostaneraCenter)
```

<!--html_preserve--><div id="htmlwidget-7ea9ac174a57f3be0e20" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-7ea9ac174a57f3be0e20">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["//{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap<\/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA<\/a>"}]},{"method":"addMarkers","args":[-33.417993,-70.60639,null,null,null,{"interactive":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},"<a href= 'http://mall.costaneracenter.cl/#map1' >Costanera Center<\/a>",null,null,null,null,{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]}],"limits":{"lat":[-33.417993,-33.417993],"lng":[-70.60639,-70.60639]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->
Now if we click the blue icon on the map, it will display Costanera Center and the link.
