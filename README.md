The reduction in passenger numbers on Ireland's domestic air routes (and getting used to SVG graphics)
=========================================================

_(This repo holds the background details for this [blog post])_

[blog post]: http://www.prockley.eu/jekyll/svg/2014/12/28/Flight-Departures-Ireland/


Currently I'm trying to get up to speed with d3.js interactive visualisations but while doing this I saw that I needed some practice getting SVG images online. This post is the result.

But it's not just about that. When I started I didn't realise that the drop off in domestic flights had been so massive. So something was learnt from the data too.


### SVG Graphics

SVG graphics are vector based and so scale nicely when people pinch to zoom on the screens of their mobile devices. They are also the typical output from d3.js interactive visualisations.


### Data Source

The data was downloaded from the website of the CSO. Only data for departing passengers was used as they would largely mirror the numbers of arriving passengers. Only data for passengers on __scheduled__ flights was used.

Most of the data wrangling was done in Excel with lookups and pivots. The relevant data is saved in CSV format in the 'data' folder.

_Source:_
[TAA02: Passenger, Freight and Commercial Flights by Airports in Ireland, Country, Direction, Flight Type, Year and Statistic](http://www.cso.ie/px/pxeirestat/Statire/SelectVarVal/Define.asp?maintable=TAA02&PLanguage=0)

_Aggregating Countries:_
There were too many countries to show on one chart so they were aggregated into regions using the [United Nations Geoscheme] as a template.

[United Nations Geoscheme]: http://en.wikipedia.org/wiki/United_Nations_geoscheme


### Generating SVG graphic

I'm new to SVG graphics and stumbled across this fantastic website for creating charts from raw data - [Raw by Density Design]. All you need to do is paste in some raw data and select the chart you want. It's a great way to see what works best initially.

[Raw by Density Design]: http://raw.densitydesign.org

I used a Bump Chart with these settings (Width: 848, Height: 500, Padding: 90, Curve: basis).

The data in '141123_DataFormatted.csv' was used. The regions 'Europe (other)' and 'Oceania & Polar' were removed due to their very small number of passengers (0.03% of the total over the whole period 2005-2013). 

Once the SVG file was generated there were some changes to be made to the underlying code to highlight the data of interest and to make sure that text was not cropped at the edges.


### Adding SVG graphic to web page

This was perhaps the most difficult part as vector graphics are harder to insert into pages than normal raster images (such as PNGs or JPEGs).

As well as inserting the images it is important that they are responsive to different screen sizes ranging from smartphones to PCs. The following blog posts on _demosthenes.info_ were very helpful:-
- [Using SVG in Web Pages][1]
- [Make SVG Responsive][2]

[1]: http://demosthenes.info/blog/428/Using-SVG-In-Web-Pages
[2]: http://demosthenes.info/blog/744/Make-SVG-Responsive
