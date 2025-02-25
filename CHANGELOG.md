# Changelog

## Unreleased

## 2.8.4 - 2024-01-31

* GetFeatureInfo - Fix a possible Python error if the item is not a `Layer` item, it can return the correct popup content

## 2.8.3 - 2024-01-29

* Fix issue about the project used when evaluating a `GetMap` request with new features from LWC 3.7

## 2.8.2 - 2024-01-15

* Fix evaluating the QGIS Drag&Drop form in a popup request when the geometry is needed, contribution from @ghtmtt

## 2.8.1 - 2023-09-27

* Support the "text widget" from QGIS 3.30 in the tooltip, contribution from @ghtmtt
* Move the fonts from the server into the JSON metadata

## 2.8.0 - 2023-07-25

* Fix concatenate with number in aggregate in the drag&drop layout popup, contribution from @ghtmtt
* For Lizmap Web Client 3.7.0 minimum
  * Add support for the "Attribute Editor Relation" when generating the tooltip
  * Add new filter for the GetLegendGraphic request
  * Add new parameter `PARENT_FEATURE` when evaluating expression

## 2.7.2 - 2023-05-30

* Fix the QGIS server name with QGIS 3.30 `'s-Hertogenbosch`

## 2.7.1 - 2023-04-13

* Add `FILTER_TYPE` to the `GETSUBSETSTRING` request with different values : `SQL` default value, `SAFESQL` or `EXPRESSION`

## 2.7.0 - 2023-03-16

* Always provide a name with the version 'not found' when fetching the list of plugin

## 1.3.1 - 2023-01-25

* Fix regression from the previous version about Py-QGIS-Server

## 1.3.0 - 2023-01-25

* Return the list of fonts installed on the server. It's useful for QGIS layouts.
* Check if Py-QGIS-Server is really used on the server before returning server metadata

## 1.2.2 - 2022-12-16

* Review the metadata and the warning when the plugin is installed on QGIS desktop
* Review the JSON metadata about Py-QGIS-Server when used with Lizmap Web Client 3.6

## 1.2.1 - 2022-11-28

* Add more metadata in the JSON about Py-QGIS-Server and QGIS Server

## 1.2.0 - 2022-10-03

* Improvement about the filtering by polygon (use a QGIS expression when possible)
* Add a new option to use the centroid for the filtering by polygon. Available in the 3.10.0 version of desktop plugin.
* Fix an issue when fetching information from `metadata.txt` in QGIS Server plugins
* Fix an issue to return Py-QGIS-Server version
* Overpass a bug from QGIS Server about a cache in WFS requests, a fix needs to be done in QGIS Server core
* All plugins versions (stable and unstable) are now available https://packages.3liz.org/pub/server-plugins-repository/

## 1.1.1 - 2022-07-29

* Add the plugin name when fetching metadata from QGIS server.
* Fix an issue when the polygon table has a schema or table name which must be enclosed with double quotes.
* Fix an issue preventing to query the PostgreSQL database to retrieve the ids to filter. Performance could be severely
  degraded for heavy filtered layers.

## 1.1.0 - 2022-07-25

* Spatial filter - Add the capability to filter spatial layers data by matching the polygon layer field values with the
  user login instead of groups only. The behaviour depends on a new configuration option `filter_by_user` for the spatial
  filter. It's compatible with Lizmap Web Client ≥ 3.5. The desktop plugin must be updated as well to version 3.9.0.

## 1.0.2 - 2022-06-28

* Refactor a little the code about access control list
* Fix an issue when the CFG file is updated and already stored in the LRU cache

## 1.0.1 - 2022-05-11

* If QGIS 3.24, use the native function from QGIS server API to fetch the feature ID
* Use LRU Cache when reading the CFG file to avoid multiple access
* Add the Python, Qt, GDAL and Py-QGIS-Server versions in the JSON metadata

## 1.0.0 - 2022-05-11

* First version of the plugin after the split between Lizmap desktop and server plugin
* The source code is the same as Lizmap plugin version 3.7.7
* Fix Python exception when GetFeatureInfo does not have a feature ID
* Raise QGIS minimum version to QGIS 3.10
