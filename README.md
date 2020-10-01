# ckanext-grouphierarchy - group hierarchy for CKAN

This CKAN extension is intended to be used in combination with the [SDDI CKAN Docker container](https://github.com/tum-gis/SDDI-CKAN-Docker).

## Overview

Provides the ability to search for datasets according to a given spatial extent. This extension is based on the [official spatial ckan extention](https://github.com/ckan/ckanext-spatial).

## Compatibility

This extension has been tested with CKAN v2.8.0 or later. 

## Installation

Install the extension in your python environment
```
$ . /usr/lib/ckan/default/bin/activate
(pyenv) $ cd /usr/lib/ckan/default/src
(pyenv) $ pip install -e "git+https://tum-gis/ckanext-spatial-sddi.git#egg=ckanext-spatial-sddi"
```
Then change your CKAN ini file (e.g. development.ini or production.ini).
```
ckan.plugins = stats text_view recline_view ... spatial
```

This extension will only work if you have the [scheming](https://github.com/tum-gis/ckanext-scheming-sddi) extension enabled. Otherwise datasets will not have the "spatial" tag and cannot be found by time search.

## Copyright & Licence

This module is Crown Copyright 2013 and openly licensed with AGPLv3 - see LICENSE file.
