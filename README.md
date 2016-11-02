# Islandora Solr Breadcrumbs

## Introduction

Islandora Solr Breadcrumbs provides a simple replacement for Sparql derived breadcrumbs.

### Caveat

This module builds a tree of Collection to Collection hierarchy, if you have Collections contained within other types of object this module will not find those relationships.

How it works is this 

The current object's content models are checked.

If it is **not** a collection, the RELS-EXT datastream is scanned for any predicates matching a list built using the [`hook_islandora_get_breadcrumb_query_predicates()`](https://github.com/Islandora/islandora/blob/7.x/islandora.api.php#L867) and followed.
  
If it **is** a collection, the cached map (is generated if it doesn't exist) is retrieved to find the parent collection quickly.

## Requirements

This module requires the following modules/libraries:

* [Islandora](https://github.com/islandora/islandora)
* [Islandora Solr](https://github.com/islandora/islandora_solr_search)
* [Tuque](https://github.com/islandora/tuque)
* [Apache Solr](https://lucene.apache.org/solr/) - 4.2 or higher.

## Installation
 
 Install as usual, see [this](https://drupal.org/documentation/install/modules-themes/modules-7) for further information.
 
## Configuration
 
To enable breadcrumbs, browse to Administration » Islandora » Configuration and choose **Islandora Solr Breadcrumbs** under **Breadcrumb generation**.

![Breadcrumbs](https://cloud.githubusercontent.com/assets/2857697/19577960/1c70a1c8-96df-11e6-8a7b-92fa16c30137.jpg)

## Troubleshooting/Issues
 
 Having problems or solved a problem? Check out the Islandora google groups for a solution.
 
 * [Islandora Group](https://groups.google.com/forum/?hl=en&fromgroups#!forum/islandora)
 * [Islandora Dev Group](https://groups.google.com/forum/?hl=en&fromgroups#!forum/islandora-dev)
 

## Maintainers/Sponsors

Current maintainers:

* [Jared Whiklo](https://github.com/whikloj)

## License

[GPLv3](http://www.gnu.org/licenses/gpl-3.0.txt)
