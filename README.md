# Jenkins Dynamic Axis Plugin

## Description

This plugin allows you to define a matrix build axis that is dynamically 
populated from an environment variable. Variables can be contributed to a 
build from a number of places, including:

- Build parameters
- Build node configuration
- Jenkins configuration
- System environment

When specifying a variable for an axis only the last category of variables can 
be validated. This is because Jenkins contributes the other types of variables
only at actual build time and thus are not available at configuration time.  

Configuring an axis is otherwise the same as for the User-defined axis option: 
specify an axis name to be used in your build along with the name of the 
environment variable to dynamically retrieve the axis values from. The rules
for the value of this variable are the same: one or more values separated by 
a space.

## Examples

Some portable environment variable names include:

- AXES
- PARAM_LIST
- 4_BUILD_CONFIG

The following are all valid values for the contents of the 
environment variable selected for an axis:

- dev tst sit
- jdk6 jdk7
- deploy_srv1 deploy_srv2 deploy_srv3

## Acknowledgements

Many thanks to Emanuele Zattin, for leading the way with the Groovy Axis
plugin. And of course to Koshuke, for continuing to improve this excellent
platform. 
