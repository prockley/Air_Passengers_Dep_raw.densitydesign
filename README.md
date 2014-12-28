The reduction in passenger numbers on Ireland's domestic air routes
======================================================

Currently I'm trying to get up to speed with d3.js interactive visualisations but while doing this I saw that I needed some practice getting SVG graphics files online. This post is the result.

SVG graphics are vector based and so scale really nicely when people get pinching on the screens of their mobile devices.


### Data Source

The data was downloaded from the website of the CSO. Only data for departing passengers was used as it was thought it would be (almost) a mirror of the arriving passenger numbers.

_Source:_
[TAA02: Passenger, Freight and Commercial Flights by Airports in Ireland, Country, Direction, Flight Type, Year and Statistic](http://www.cso.ie/px/pxeirestat/Statire/SelectVarVal/Define.asp?maintable=TAA02&PLanguage=0)

_Aggregating Countries:_
There were too many countries to show on one chart so they were aggregated into regions using the [United Nations Geoscheme] as a template.

[United Nations Geoscheme]: http://en.wikipedia.org/wiki/United_Nations_geoscheme


### Generating SVG graphic

I'm new to SVG graphics and stumbled across this fantastic website for creating charts from raw data - [Raw by Density Design]. All you need to do is paste in some raw data and select the chart you want. It's a great way to see what works best initially.

[Raw by Density Design]: http://raw.densitydesign.org

I used a Bump Chart with these settings (Width: 848, Height: 500, Padding: 90, Curve: basis).

Once the SVG files were generated there were some changes to be made to the underlying code to highlight the data of interest and to make sure that text was not cropped at the edges.


### Adding SVG graphic to web page

This was perhaps the most difficult part as vector graphics are harder to insert into pages than normal raster images (such as PNGs or JPEGs).

As well as inserting the images it is important that they are responsive to different screen sizes ranging from smartphones to PCs. The following blog posts on _demosthenes.info_ were very helpful:-
- [Using SVG in Web Pages][1]
- [Make SVG Responsive][2]

[1]: http://demosthenes.info/blog/428/Using-SVG-In-Web-Pages
[2]: http://demosthenes.info/blog/744/Make-SVG-Responsive
