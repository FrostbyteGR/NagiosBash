# NagiosBash

## I. DESCRIPTION:

A collection of Linux nagios plugins written in bash

Copyright (c) 2019 Frostbyte <frostbytegr@gmail.com>

## II. CREDITS:

* github.com/hugme - sample code for linux nagios checks
* devel@nagios-plugins.org - plugin development guidelines

## III. FEATURES:

* Output includes perfdata
* Any warning and critical thresholds may be fully or partially omitted
  - Anything that has not been explicitly specified will be disabled
* No extra packages or external programs are required for operation

## IV. USAGE:

* check_cpu [-w util_warn_threshold] [-c util_warn_threshold]
  - example: check_cpu -w 80 -c 90
* check_cputemp [-w temp_warn_threshold] [-c temp_warn_threshold]
  - example: check_cputemp -w 65 -c 70
  - NOTE: Does not support negative threshold values
* check_memory [-w util_warn_threshold] [-c util_warn_threshold] [-u friendly_unit] [-n]
  - friendly units: K=Kilobytes, M=Megabytes, G=Gigabytes, T=Terabytes
  - example: check_memory -w 80 -c 90 -u M
  - NOTE: Cached memory and buffers will not be included in system's free memory when calculating utilization, with the -n argument
* check_uptime
  - NOTE: Does not support warning/critical states
