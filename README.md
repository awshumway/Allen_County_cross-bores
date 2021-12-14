# Allen County Cross-bores

Using raw data and limited information, create an analysis for Allen County, Indiana which includes a map of high-risk streets and a driving route for a field crew.

Source data can be found in /src_data

## Mapbox Interactive Map

[Interactive Map of Allen County pipe data](https://api.mapbox.com/styles/v1/awshum/ckx4a953k5xnc14kzqn3wipiu.html?title=view&access_token=pk.eyJ1IjoiYXdzaHVtIiwiYSI6ImNreDJtODNiMTFramYycnQ5aG1uejVncDAifQ._Mwl7bk0McztwyCfvyTG3g&zoomwheel=true&fresh=true#12.24/41.07561/-85.13472)

## Understanding the data

GISMAPSTREET.txt as provided has 15 columns:

| Column Name           | Description                                               |
| --------------------- | --------------------------------------------------------- |
| MINORGRIDNAME         | Minor Grid Name, seems to be a custom name or identifier  |
| STREETNAME            | Name of the street, such as "Gordon Rd"                   |
| ROADDIRECTIONPREFIXCD | Prefix road direction, such as N for North                |
| ROADNAME              | Name of the Road, such as "Gordon"                        |
| ROADTYPESUFFIXCD      | Type of road code, such as ST, RD, LN, etc.               |
| ROADDIRECTIONSUFFIXCD | Suffix road direction, such as W for West                 |
| LEFTZIPCD             | Left Zip Code                                             |
| RIGHTZIPCD            | Right Zip Code                                            |
| LOWADDRESSRANGEVALUE  | Value for the lowest/ first address on the street         |
| HIGHADDRESSRANGEVALUE | Value for the highest/ last address on the street         |
| TOWNSHIPNAME          | Name of the township where the street is located          |
| MUNICIPALITYNAME      | Name of the municipality in which the township is located |
| NUMCENTERLINES        | The number of centerlines found on the street             |
| INTERSECTINGLENGTH    | Intersecting Length                                       |
| GEOM_WKT              | Geometry Well-known text                                  |

Street Consequence has 5 columns:

| Column Name        | Description                                                                  |
| ------------------ | ---------------------------------------------------------------------------- |
| STATE              | Address State two-letter code, such as IN                                    |
| MUNICIPALITY       | name of the municipality in which the street is located                      |
| STREETNAME         | Name of the street                                                           |
| MINORGRIDNAME      | Minor Grid Name, custom name or ID?                                          |
| Street Consequence | Consequence associated with the street, greater number = greater consequence |

## Helpful Mapbox Links

* [Get started with Mapbox GL JS expressions](https://docs.mapbox.com/help/tutorials/mapbox-gl-js-expressions/#set-up-a-map)
* [Mapbox Style Spec Data Expressions](https://docs.mapbox.com/mapbox-gl-js/style-spec/expressions/#data-expressions)
* [Recipe Basics](https://docs.mapbox.com/mapbox-tiling-service/examples/basic-recipe-using-zoom-levels/)
* [API uploads](https://docs.mapbox.com/api/maps/uploads/)

## Next Steps

1. Use a recipe to specify min and max zoom for the tileset to address zoom issues
2. Improve wrangling code processing time
3. Add functions to ETL pipeline code to improve readability
4. Discover why some streets seem to have multiple different consequence values

## Notes

Initial test Tileset ID : awshum.75w3tcn9
Full tileset ID : awshum.allen-co-pipes
