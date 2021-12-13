# Allen County Cross-bores

Using raw data and limited information, create an analysis for Allen County, Indiana which includes a map of high-risk streets and a driving route for a field crew.

Source data can be found in /src_data

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
